## API Report File for "@aws-amplify/graphql-transformer"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AppSyncAuthConfiguration } from '@aws-amplify/graphql-transformer-interfaces';
import { AssetProvider } from '@aws-amplify/graphql-transformer-interfaces';
import { Construct } from 'constructs';
import type { DataSourceStrategiesProvider } from '@aws-amplify/graphql-transformer-interfaces';
import { GraphQLTransform } from '@aws-amplify/graphql-transformer-core';
import { IFunction } from 'aws-cdk-lib/aws-lambda';
import { NestedStackProvider } from '@aws-amplify/graphql-transformer-interfaces';
import type { RDSLayerMappingProvider } from '@aws-amplify/graphql-transformer-interfaces';
import { ResolverConfig } from '@aws-amplify/graphql-transformer-core';
import { SynthParameters } from '@aws-amplify/graphql-transformer-interfaces';
import { TransformerLog } from '@aws-amplify/graphql-transformer-interfaces';
import { TransformerPluginProvider } from '@aws-amplify/graphql-transformer-interfaces';
import { TransformParameterProvider } from '@aws-amplify/graphql-transformer-interfaces';
import type { TransformParameters } from '@aws-amplify/graphql-transformer-interfaces';
import { UserDefinedSlot } from '@aws-amplify/graphql-transformer-core';

// @public (undocumented)
export const constructTransform: (config: TransformConfig) => GraphQLTransform;

// @public (undocumented)
export const constructTransformerChain: (options?: TransformerFactoryArgs) => TransformerPluginProvider[];

// @public (undocumented)
export const executeTransform: (config: ExecuteTransformConfig) => void;

// @public (undocumented)
export type ExecuteTransformConfig = TransformConfig & DataSourceStrategiesProvider & RDSLayerMappingProvider & {
    schema: string;
    printTransformerLog?: (log: TransformerLog) => void;
    scope: Construct;
    nestedStackProvider: NestedStackProvider;
    parameterProvider?: TransformParameterProvider;
    assetProvider: AssetProvider;
    synthParameters: SynthParameters;
};

// @public (undocumented)
export type TransformConfig = {
    transformersFactoryArgs: TransformerFactoryArgs;
    resolverConfig?: ResolverConfig;
    authConfig?: AppSyncAuthConfiguration;
    userDefinedSlots?: Record<string, UserDefinedSlot[]>;
    stackMapping?: Record<string, string>;
    transformParameters: TransformParameters;
};

// @public (undocumented)
export type TransformerFactoryArgs = {
    storageConfig?: any;
    customTransformers?: TransformerPluginProvider[];
    functionNameMap?: Record<string, IFunction>;
};

// (No @packageDocumentation comment for this package)

```
