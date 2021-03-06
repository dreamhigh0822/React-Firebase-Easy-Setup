---
title: React Realtime Database
sidebar_label: API
---

- [FirebaseDatabaseProvider Props](#firebasedatabaseprovider-props)
- [Firebase Setup Reference](#firebase-setup-reference)
- [FirebaseDatabaseNode Props](#firebasedatabasenode-props)
- [Firebase Query Reference](#firebase-query-reference)
- [FirebaseDatabaseMutation Props](#firebasedatabasemutation-props)
- [Firebase Write Data Reference](#firebase-write-data-reference)
- [FirebaseDatabaseTransaction Props](#firebasedatabasetransaction-props)
- [Firebase Transaction Reference](#firebase-transaction-reference)

## FirebaseDatabaseProvider Props

| Name              | Type                                               | Required | Default |
| :---------------- | :------------------------------------------------- | :------- | :------ |
| firebase          | [firebase](https://www.npmjs.com/package/firebase) | no       |         |
| authDomain        | string                                             | yes      |         |
| apiKey            | string                                             | yes      |         |
| databaseURL       | string                                             | yes      |         |
| projectId         | string                                             | yes      |         |
| messagingSenderId | string                                             | no       |         |
| storageBucket     | string                                             | no       |         |
| children          | React Node                                         | no       |         |
| render            | () => ReactNode                                    | no       |         |

## [Firebase Setup Reference](https://firebase.google.com/docs/database/web/start)

## FirebaseDatabaseNode Props



| Name         | Type                                                        | Required | Default |
| :----------- | :---------------------------------------------------------- | :------- | :------ |
| path         | string                                                      | yes      |         |
| orderByChild | string                                                      | no       | null    |
| orderByValue | any                                                         | no       | null    |
| orderByKey   | any                                                         | yes      | null    |
| limitToFirst | number                                                      | no       | null    |
| limitToLast  | number                                                      | no       | null    |
| startAt      | number                                                      | no       | null    |
| endAt        | number                                                      | no       | null    |
| equalTo      | any                                                         | no       | null    |
| children     | ({path:string, isLoading,:boolean, value:any}) => ReactNode | no       | null    |

## [Firebase Query Reference](https://firebase.google.com/docs/database/admin/retrieve-data#section-queries)

## FirebaseDatabaseMutation Props



| Name     | Type                                                                    | Required | Default |
| :------- | :---------------------------------------------------------------------- | :------- | :------ |
| path     | string                                                                  | yes      |         |
| type     | `set` or `update` or `push`                                             | yes      |         |
| children | ( { runMutation: (value:any) => Promise<{key?:string}> } ) => ReactNode | yes      | null    |

## [Firebase Write Data Reference](https://firebase.google.com/docs/database/web/read-and-write#reading_and_writing_data)

## FirebaseDatabaseTransaction Props



| Name     | Type                                                                                   | Required | Default |
| :------- | :------------------------------------------------------------------------------------- | :------- | :------ |
| path     | string                                                                                 | yes      |         |
| children | ( { runTransaction: ({ reducer: (val:any) => any }) => Promise\<void> } ) => ReactNode | yes      | null    |

## [Firebase Transaction Reference](https://firebase.google.com/docs/database/web/read-and-write#save_data_as_transactions)



