<!--- Hugo front matter used to generate the website version of this page:
linkTitle: AWS DynamoDB
--->

# Semantic Conventions for AWS DynamoDB

**Status**: [Experimental][DocumentStatus]

The Semantic Conventions for [AWS DynamoDB](https://aws.amazon.com/dynamodb/) extend and override the general
[AWS SDK Semantic Conventions](/docs/cloud-providers/aws-sdk.md)
that describe common AWS SDK attributes and the [Database Semantic Conventions](database-spans.md).
that describe common database operations attributes in addition to the Semantic Conventions
described on this page.

## Common Attributes

These attributes are filled in for all DynamoDB request types.

<!-- semconv dynamodb.all(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`db.system`](/docs/attributes-registry/db.md) | string | The value `dynamodb`. | `dynamodb` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

`db.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `other_sql` | Some other SQL database. Fallback only. See notes. | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `mssql` | Microsoft SQL Server | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `mssqlcompact` | Microsoft SQL Server Compact | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `mysql` | MySQL | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `oracle` | Oracle Database | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `db2` | IBM Db2 | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `postgresql` | PostgreSQL | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `redshift` | Amazon Redshift | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `hive` | Apache Hive | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `cloudscape` | Cloudscape | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `hsqldb` | HyperSQL DataBase | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `progress` | Progress Database | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `maxdb` | SAP MaxDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `hanadb` | SAP HANA | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `ingres` | Ingres | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `firstsql` | FirstSQL | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `edb` | EnterpriseDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `cache` | InterSystems Caché | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `adabas` | Adabas (Adaptable Database System) | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `firebird` | Firebird | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `derby` | Apache Derby | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `filemaker` | FileMaker | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `informix` | Informix | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `instantdb` | InstantDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `interbase` | InterBase | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `mariadb` | MariaDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `netezza` | Netezza | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `pervasive` | Pervasive PSQL | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `pointbase` | PointBase | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `sqlite` | SQLite | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `sybase` | Sybase | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `teradata` | Teradata | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `vertica` | Vertica | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `h2` | H2 | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `coldfusion` | ColdFusion IMQ | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `cassandra` | Apache Cassandra | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `hbase` | Apache HBase | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `mongodb` | MongoDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `redis` | Redis | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `couchbase` | Couchbase | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `couchdb` | CouchDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `cosmosdb` | Microsoft Azure Cosmos DB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dynamodb` | Amazon DynamoDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `neo4j` | Neo4j | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `geode` | Apache Geode | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `elasticsearch` | Elasticsearch | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `memcached` | Memcached | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `cockroachdb` | CockroachDB | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `opensearch` | OpenSearch | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `clickhouse` | ClickHouse | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `spanner` | Cloud Spanner | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `trino` | Trino | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.BatchGetItem

<!-- semconv dynamodb.batchgetitem(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | The keys in the `RequestItems` object field. | `Users`; `Cats` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.BatchWriteItem

<!-- semconv dynamodb.batchwriteitem(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.item_collection_metrics`](/docs/attributes-registry/aws.md) | string | The JSON-serialized value of the `ItemCollectionMetrics` response field. | `{ "string" : [ { "ItemCollectionKey": { "string" : { "B": blob, "BOOL": boolean, "BS": [ blob ], "L": [ "AttributeValue" ], "M": { "string" : "AttributeValue" }, "N": "string", "NS": [ "string" ], "NULL": boolean, "S": "string", "SS": [ "string" ] } }, "SizeEstimateRangeGB": [ number ] } ] }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | The keys in the `RequestItems` object field. | `Users`; `Cats` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.CreateTable

<!-- semconv dynamodb.createtable(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.global_secondary_indexes`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item of the `GlobalSecondaryIndexes` request field | `{ "IndexName": "string", "KeySchema": [ { "AttributeName": "string", "KeyType": "string" } ], "Projection": { "NonKeyAttributes": [ "string" ], "ProjectionType": "string" }, "ProvisionedThroughput": { "ReadCapacityUnits": number, "WriteCapacityUnits": number } }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.item_collection_metrics`](/docs/attributes-registry/aws.md) | string | The JSON-serialized value of the `ItemCollectionMetrics` response field. | `{ "string" : [ { "ItemCollectionKey": { "string" : { "B": blob, "BOOL": boolean, "BS": [ blob ], "L": [ "AttributeValue" ], "M": { "string" : "AttributeValue" }, "N": "string", "NS": [ "string" ], "NULL": boolean, "S": "string", "SS": [ "string" ] } }, "SizeEstimateRangeGB": [ number ] } ] }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.local_secondary_indexes`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item of the `LocalSecondaryIndexes` request field. | `{ "IndexArn": "string", "IndexName": "string", "IndexSizeBytes": number, "ItemCount": number, "KeySchema": [ { "AttributeName": "string", "KeyType": "string" } ], "Projection": { "NonKeyAttributes": [ "string" ], "ProjectionType": "string" } }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.provisioned_read_capacity`](/docs/attributes-registry/aws.md) | double | The value of the `ProvisionedThroughput.ReadCapacityUnits` request parameter. | `1`; `2` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.provisioned_write_capacity`](/docs/attributes-registry/aws.md) | double | The value of the `ProvisionedThroughput.WriteCapacityUnits` request parameter. | `1`; `2` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.DeleteItem

<!-- semconv dynamodb.deleteitem(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.item_collection_metrics`](/docs/attributes-registry/aws.md) | string | The JSON-serialized value of the `ItemCollectionMetrics` response field. | `{ "string" : [ { "ItemCollectionKey": { "string" : { "B": blob, "BOOL": boolean, "BS": [ blob ], "L": [ "AttributeValue" ], "M": { "string" : "AttributeValue" }, "N": "string", "NS": [ "string" ], "NULL": boolean, "S": "string", "SS": [ "string" ] } }, "SizeEstimateRangeGB": [ number ] } ] }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.DeleteTable

<!-- semconv dynamodb.deletetable(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.DescribeTable

<!-- semconv dynamodb.describetable(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.GetItem

<!-- semconv dynamodb.getitem(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consistent_read`](/docs/attributes-registry/aws.md) | boolean | The value of the `ConsistentRead` request parameter. |  | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.projection`](/docs/attributes-registry/aws.md) | string | The value of the `ProjectionExpression` request parameter. | `Title`; `Title, Price, Color`; `Title, Description, RelatedItems, ProductReviews` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.ListTables

<!-- semconv dynamodb.listtables(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.exclusive_start_table`](/docs/attributes-registry/aws.md) | string | The value of the `ExclusiveStartTableName` request parameter. | `Users`; `CatsTable` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.limit`](/docs/attributes-registry/aws.md) | int | The value of the `Limit` request parameter. | `10` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_count`](/docs/attributes-registry/aws.md) | int | The number of items in the `TableNames` response parameter. | `20` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.PutItem

<!-- semconv dynamodb.putitem(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.item_collection_metrics`](/docs/attributes-registry/aws.md) | string | The JSON-serialized value of the `ItemCollectionMetrics` response field. | `{ "string" : [ { "ItemCollectionKey": { "string" : { "B": blob, "BOOL": boolean, "BS": [ blob ], "L": [ "AttributeValue" ], "M": { "string" : "AttributeValue" }, "N": "string", "NS": [ "string" ], "NULL": boolean, "S": "string", "SS": [ "string" ] } }, "SizeEstimateRangeGB": [ number ] } ] }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | The keys in the `RequestItems` object field. | `Users`; `Cats` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.Query

<!-- semconv dynamodb.query(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.attributes_to_get`](/docs/attributes-registry/aws.md) | string[] | The value of the `AttributesToGet` request parameter. | `lives`; `id` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consistent_read`](/docs/attributes-registry/aws.md) | boolean | The value of the `ConsistentRead` request parameter. |  | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.index_name`](/docs/attributes-registry/aws.md) | string | The value of the `IndexName` request parameter. | `name_to_group` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.limit`](/docs/attributes-registry/aws.md) | int | The value of the `Limit` request parameter. | `10` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.projection`](/docs/attributes-registry/aws.md) | string | The value of the `ProjectionExpression` request parameter. | `Title`; `Title, Price, Color`; `Title, Description, RelatedItems, ProductReviews` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.scan_forward`](/docs/attributes-registry/aws.md) | boolean | The value of the `ScanIndexForward` request parameter. |  | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.select`](/docs/attributes-registry/aws.md) | string | The value of the `Select` request parameter. | `ALL_ATTRIBUTES`; `COUNT` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.Scan

<!-- semconv dynamodb.scan(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.attributes_to_get`](/docs/attributes-registry/aws.md) | string[] | The value of the `AttributesToGet` request parameter. | `lives`; `id` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consistent_read`](/docs/attributes-registry/aws.md) | boolean | The value of the `ConsistentRead` request parameter. |  | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.count`](/docs/attributes-registry/aws.md) | int | The value of the `Count` response parameter. | `10` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.index_name`](/docs/attributes-registry/aws.md) | string | The value of the `IndexName` request parameter. | `name_to_group` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.limit`](/docs/attributes-registry/aws.md) | int | The value of the `Limit` request parameter. | `10` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.projection`](/docs/attributes-registry/aws.md) | string | The value of the `ProjectionExpression` request parameter. | `Title`; `Title, Price, Color`; `Title, Description, RelatedItems, ProductReviews` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.scanned_count`](/docs/attributes-registry/aws.md) | int | The value of the `ScannedCount` response parameter. | `50` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.segment`](/docs/attributes-registry/aws.md) | int | The value of the `Segment` request parameter. | `10` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.select`](/docs/attributes-registry/aws.md) | string | The value of the `Select` request parameter. | `ALL_ATTRIBUTES`; `COUNT` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.total_segments`](/docs/attributes-registry/aws.md) | int | The value of the `TotalSegments` request parameter. | `100` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.UpdateItem

<!-- semconv dynamodb.updateitem(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.item_collection_metrics`](/docs/attributes-registry/aws.md) | string | The JSON-serialized value of the `ItemCollectionMetrics` response field. | `{ "string" : [ { "ItemCollectionKey": { "string" : { "B": blob, "BOOL": boolean, "BS": [ blob ], "L": [ "AttributeValue" ], "M": { "string" : "AttributeValue" }, "N": "string", "NS": [ "string" ], "NULL": boolean, "S": "string", "SS": [ "string" ] } }, "SizeEstimateRangeGB": [ number ] } ] }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

## DynamoDB.UpdateTable

<!-- semconv dynamodb.updatetable(full) -->
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`rpc.system`](/docs/attributes-registry/rpc.md) | string | The value `aws-api`. | `aws-api` | `Required` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.attribute_definitions`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `AttributeDefinitions` request field. | `{ "AttributeName": "string", "AttributeType": "string" }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.consumed_capacity`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `ConsumedCapacity` response field. | `{ "CapacityUnits": number, "GlobalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "LocalSecondaryIndexes": { "string" : { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number } }, "ReadCapacityUnits": number, "Table": { "CapacityUnits": number, "ReadCapacityUnits": number, "WriteCapacityUnits": number }, "TableName": "string", "WriteCapacityUnits": number }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.global_secondary_index_updates`](/docs/attributes-registry/aws.md) | string[] | The JSON-serialized value of each item in the `GlobalSecondaryIndexUpdates` request field. | `{ "Create": { "IndexName": "string", "KeySchema": [ { "AttributeName": "string", "KeyType": "string" } ], "Projection": { "NonKeyAttributes": [ "string" ], "ProjectionType": "string" }, "ProvisionedThroughput": { "ReadCapacityUnits": number, "WriteCapacityUnits": number } }` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.provisioned_read_capacity`](/docs/attributes-registry/aws.md) | double | The value of the `ProvisionedThroughput.ReadCapacityUnits` request parameter. | `1`; `2` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.provisioned_write_capacity`](/docs/attributes-registry/aws.md) | double | The value of the `ProvisionedThroughput.WriteCapacityUnits` request parameter. | `1`; `2` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.dynamodb.table_names`](/docs/attributes-registry/aws.md) | string[] | A single-element array with the value of the TableName request parameter. | `Users` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`aws.request_id`](/docs/attributes-registry/aws.md) | string | The AWS request ID as returned in the response headers `x-amz-request-id` or `x-amz-requestid`. | `79b9da39-b7ae-508a-a6bc-864b2829c622`; `C9ER4AJX75574TDJ` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.method`](/docs/attributes-registry/rpc.md) | string | The name of the operation corresponding to the request, as returned by the AWS SDK [1] | `GetItem`; `PutItem` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| [`rpc.service`](/docs/attributes-registry/rpc.md) | string | The name of the service to which a request is made, as returned by the AWS SDK. [2] | `DynamoDB`; `S3` | `Recommended` | ![Experimental](https://img.shields.io/badge/-experimental-blue) |

**[1]:** This is the logical name of the method from the RPC interface perspective, which can be different from the name of any implementing method/function. The `code.function` attribute may be used to store the latter (e.g., method actually executing the call on the server side, RPC client stub method on the client side).

**[2]:** This is the logical name of the service from the RPC interface perspective, which can be different from the name of any implementing class. The `code.namespace` attribute may be used to store the latter (despite the attribute name, it may include a class name; e.g., class with method actually executing the call on the server side, RPC client stub class on the client side).

`rpc.system` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `grpc` | gRPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `java_rmi` | Java RMI | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `dotnet_wcf` | .NET WCF | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `apache_dubbo` | Apache Dubbo | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
| `connect_rpc` | Connect RPC | ![Experimental](https://img.shields.io/badge/-experimental-blue) |
<!-- endsemconv -->

[DocumentStatus]: https://github.com/open-telemetry/opentelemetry-specification/tree/v1.31.0/specification/document-status.md
