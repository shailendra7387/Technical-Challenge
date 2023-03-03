PowerShell Script

Invoke-RestMethod -Method GET -uri "http://xyz/metadata/instance?api-version=0.1" -Headers $MetaDataHeaders 


Let's say if you want have finf specific tags 
curl -H Metadata:true --noproxy "*" "http://xyz/metadata/instance?api-version=0.1" | jq '.compute.tagsList[] | select(.name=="Creator") | .value'