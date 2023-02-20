# Configuring your DNS server

To set up Garage on your domain, you'd need to do some DNS configuration.

## DNS settings example

The DNS setup is dependent on your actual layout. The following example shows two servers.
On both servers runs a gateway (gw). Server1 has two nodes as e.g. it has two drives while server2 has one node

| Type  | Host                       | Priority | Weight | Port | Target                   |
|-------|----------------------------|----------|--------|------|--------------------------|
| A     | `garage-gw1.example.com`   | -        | -      | -    | `IP server1`             |
| CNAME | `garage-node1.example.com` | -        | -      | -    | `garage-gw1.example.com` |
| CNAME | `garage-node2.example.com` | -        | -      | -    | `garage-gw1.example.com` |
| A     | `garage-gw2.example.com`   | -        | -      | -    | `IP server2`             |
| CNAME | `garage-node3.example.com` | -        | -      | -    | `garage-gw2.example.com` |

Be mindful as to how long it will take for the DNS records to propagate.

When you're done configuring DNS, proceed to [Configuring the playbook](configuring-playbook.md).
