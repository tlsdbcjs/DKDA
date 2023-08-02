# SMB NFS 구성 시 하기 nfs external 설치 필수

# 사전에 NFS 서버의 /etc/export에 해당 폴더 권한이 설정 필요함
helm install nfs-client-smb-server nfs-subdir-external-provisioner/nfs-subdir-external-provisioner \
	--namespace {{ default }} \
	--set nfs.server={{ 192.168.10.171 }} \
	--set nfs.path={{ /nfs/default }} \
	--set storageClass.name=nfs-client-smb-server
