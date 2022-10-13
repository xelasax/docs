---
slug: /solana/react.useminttoken
title: useMintToken() function
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## useMintToken() function

Mint tokens on your token program

## Example

```jsx
import { useProgram, useMintToken } from "@thirdweb-dev/react/solana";

export default function Component() {
  const { program } = useProgram("{{program_address}}");
  const { mutateAsync: mint, isLoading, error } = useMintToken(program);

  return (
    <button onClick={() => mint({ to: "{{wallet_address}}", amount: 1 })}>
      Mint
    </button>
  );
}
```

**Signature:**

```typescript
export declare function useMintToken(
  program: RequiredParam<Token>,
): import("@tanstack/react-query").UseMutationResult<
  import("@thirdweb-dev/sdk/solana").TransactionResult,
  unknown,
  TokenParams,
  unknown
>;
```

## Parameters

| Parameter | Type                       | Description                                    |
| --------- | -------------------------- | ---------------------------------------------- |
| program   | RequiredParam&lt;Token&gt; | The program instance of the program to mint on |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;import("@thirdweb-dev/sdk/solana").TransactionResult, unknown, TokenParams, unknown&gt;