```
pdnsutil create-zone yzguy.local
pdnsutil set-kind yzguy.local master
pdnsutil set-meta yzguy.local ALLOW-AXFR-FROM 172.19.0.0/24
pdnsutil set-meta yzguy.local ALSO-NOTIFY 172.19.0.3
pdnsutil add-record yzguy.local ns1 A 300 172.19.0.3
pdnsutil add-record yzguy.local @ NS 300 ns1.yzguy.local.
pdnsutil increase-serial yzguy.local
pdnsutil show-zone yzguy.local
```
