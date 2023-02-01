---
slug: /react.userevokerole
title: useRevokeRole() function
hide_title: true
displayed_sidebar: react
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## useRevokeRole() function

> This feature is currently in beta and may change based on feedback that we receive.

Use this to revoke a [WalletAddress](./react.walletaddress.md) a specific role on a

## Example

```jsx
const Component = () => {
  const { mutate: revokeRole, isLoading, error } = useRevokeRole(SmartContract);

  if (error) {
    console.error("failed to revoke role", error);
  }

  return (
    <button
      disabled={isLoading}
      onClick={() => revokeRole({ role: "admin", address: "0x123" })}
    >
      Revoke Role
    </button>
  );
};
```

**Signature:**

```typescript
export declare function useRevokeRole<TContract extends ContractWithRoles>(
  contract: RequiredParam<TContract>,
): import("@tanstack/react-query").UseMutationResult<
  void,
  unknown,
  {
    role: RolesForContract<TContract>;
    address: WalletAddress;
  },
  unknown
>;
```

## Parameters

| Parameter | Type                                                       | Description      |
| --------- | ---------------------------------------------------------- | ---------------- |
| contract  | [RequiredParam](./react.requiredparam.md)&lt;TContract&gt; | an instance of a |

**Returns:**

import("@tanstack/react-query").UseMutationResult&lt;void, unknown, { role: RolesForContract&lt;TContract&gt;; address: [WalletAddress](./react.walletaddress.md); }, unknown&gt;

a mutation object that can be used to revoke a role from a member on the contract