# pvea-proxmox
pvea-proxmox (pronounced pea-va) is a modern and up-to-date node.js client for the proxmox api. Note: This is a reupload of pvea package of Jade Cole! 

###### [Proxmox API wiki.](https://pve.proxmox.com/wiki/Proxmox_VE_API)
###### [Proxmox API documentation.](https://pve.proxmox.com/pve-docs/api-viewer/index.html)

## Installation:

  `npm i pvea-proxmox` or  `yarn add pvea-proxmox`.


## To-Do List:

- [X] Basic functionality.
    - [X] Authenticate with Proxmox VE API.
    - [X] Check if authentication token is expired.
    - [X] Get api version.

- [X] storage
    - [X] getStorage(param)
    - [X] createStorage(param)
    - [X] getStorageConfig(storage)
    - [X] deleteStorageConfig(storage, param)
    - [X] getStorageStatus(node, storage)
    - [X] getStorageRrdData(node, storage, param)
    - [X] getStorageContent(node, storage, param)
    - [X] allocateDiskImage(node, storage, param)
    - [X] getVolumeAttributes(node, storage, volume, param)
    - [X] deleteVolume(node, storage, volume, param)
    - [X] createBackup(node, param)
    - [X] getBackupConfig(node, param)

- [X] pools
    - [X] getPools()
    - [X] getPoolConfig(poolid)
    - [X] deletePoolConfig(poolid)
    - [X] updatePoolConfig(poolid, param)

- [X] nodes
    - [X] getNodes()
    - [X] wakeNode(node)
    - [X] getNodeVersion(node)
    - [X] getNodeTime(node)
    - [X] updateNodeTimeZone(node, param)
    - [X] getNodeLog(node, param)
    - [X] getNodeSubscriptionStatus(node)
    - [X] deleteNodeSubscriptionKey(node)
    - [X] setNodeSubscriptionKey(node)
    - [X] updateNodeSubscriptionKey(node)
    - [X] stopAll(node, param)
    - [X] getNodeStatus(node)
    - [X] rebootNode(node)
    - [X] shutdownNode(node)
    - [X] startAll(node, param)
    - [X] getNodeRrdData(node)
    - [X] getNodeReport(node)
    - [X] getNodeNetstat(node)
    - [X] migrateAll(node, param)
    - [X] getNodeJournal(node, param)
    - [X] getNodeHostname(node)
    - [X] setNodeHostname(node, param)
    - [X] getNodeDnsSettings(node)
    - [X] setNodeDnsSettings(node, param)
    - [X] listNodeCpu(node)
    - [X] getNodeConfig(node, param)
    - [X] updateNodeConfig(node, param)
    - [X] getNodeAplInfo(node)


- [X] tasks
    - [X] getNodeTasks(node, param)
    - [X] stopTask(node, upid)
    - [X] getTaskLog(node, upid, param)
    - [X] getTaskStatus(node, upid)

- [X] services
    - [X] reloadService(node, service)
    - [X] restartService(node, service)
    - [X] startService(node, service)
    - [X] stopService(node, service)
    - [X] getServiceState(node, service)
    - [X] listServices(node)

- [X] lxc
    - [X] listLxcContainers(node)
    - [X] createLxcContainer(node, param)
    - [X] createLxcTemplate(node, vmid)
    - [X] getLxcRRDData(node, vmid, param)
    - [X] resizeLxcContainer(node, vmid, param)
    - [X] getLxcPending(node, vmid)
    - [X] getLxcConfig(node, vmid)
    - [X] cloneLxcContainer(node, vmid, param)
    - [X] suspendLxcContainer(node, vmid)
    - [X] stopLxcContainer(node, vmid)
    - [X] resumeLxcContainer(node, vmid)
    - [X] rebootLxcContainer(node, vmid)
    - [X] getLxcContainerStatus(node, vmid)
    - [X] deleteLxcContainer(node, vmid, param)
    - [X] getLxcSnapshot(node, vmid)
    - [X] createLxcSnapshot(node, vmid, param)
    - [X] deleteLxcSnapshot(node, vmid, snapName, param)
    - [X] getLxcSnapshotConfig(node, vmid, snapName)
    - [X] updateLxcSnapshotMetadata(node, vmid, snapName, param)
    - [X] rollbackLxcContainer(node, vmid, snapName)
    - [X] getLxcFirewallRefs(node, vmid)
    - [X] getLxcFirewallOptions(node, vmid)
    - [X] setLxcFirewallOptions(node, vmid, param)
    - [X] getLxcFirewallLog(node, vmid, param)
    - [X] getLxcFirewallRules(node, vmid)
    - [X] createLxcFirewallRule(node, vmid, param)
    - [X] getLxcFirewallIPSets(node, vmid)
    - [X] createLxcFirewallIPSet(node, vmid, param)
    - [X] getLxcFirewallAliases(node, vmid)
    - [X] createLxcFirewallAlias(node, vmid, param)
- [X] qemu
    - [X] listQemuVms(node)
    - [X] getQemuVmConfig(node, vmid)
    - [X] checkQemuVmFeature(node, vmid)
    - [X] getQemuVmMigrationPreconditions(node, vmid)
    - [X] cloneQemuVm(node, vmid, param)
    - [X] suspendQemuVm(node, vmid)
    - [X] stopQemuVm(node, vmid)
    - [X] startQemuVm(node, vmid)
    - [X] shutdownQemuVm(node, vmid)
    - [X] resumeQemuVm(node, vmid)
    - [X] rebootQemuVm(node, vmid)
    - [X] execQemuMonitorCommand(node, vmid, param)
    - [X] moveQemuVmDisk(node, vmid, param)
    - [X] getQemuVmPendingConfig(node, vmid)
    - [X] getQemuSnapshot(node, vmid)
    - [X] createQemuSnapshot(node, vmid, param)
    - [X] deleteQemuSnapshot(node, vmid, snapName, param)
    - [X] getQemuSnapshotConfig(node, vmid, snapName)
    - [X] updateQemuSnapshotMetadata(node, vmid, snapName, param)
    - [X] rollbackQemuVm(node, vmid, snapName)
    - [X] createQemuVm(node, param)
    - [X] getQemuVmCloudinitConfig(node, vmid)
    - [X] makeQemuVmTemplate(node, vmid, param)
    - [X] createQemuVmTermProxy(node, vmid, param)
    - [X] getQemuFirewallRefs(node, vmid)
    - [X] getQemuFirewallOptions(node, vmid)
    - [X] setQemuFirewallOptions(node, vmid, param)
    - [X] getQemuFirewallLog(node, vmid, param)
    - [X] getQemuFirewallRules(node, vmid)
    - [X] createQemuFirewallRule(node, vmid, param)
    - [X] getQemuFirewallIPSets(node, vmid)
    - [X] createQemuFirewallIPSet(node, vmid, param)
    - [X] createQemuFirewallIPSet(node, vmid, param)
    - [X] unlinkQemuVmDisk(node, vmid, param)
    - [X] createQemuVmVncProxy(node, vmid, param)
    - [X] getQemuRRDData(node, vmid, param)
    - [X] execGetQemuAgentCommand(node, vmid, command)
    - [X] execPostQemuAgentCommand(node, vmid, command, params)
    - [X] deleteQemuVm(node, vmid, param) 
    - [X] getCurrentQemuVmState(node, vmid)
- [ ] Write documentation for this library.

## Example:

    // pvea library.
    const pveajs = require("pvea")

    // create a new instance, you can use this to connect to multiple nodes if you want.
    const pvea = new pveajs('hostname', 'user@auth', 'password')

    // our main application.
    async function main() {
        // get version of proxmox API.
        pvea.apiVersion().then( res => {
            // log result.
            console.log(res)
        })
    }

    // execute the application.
    pvea.run(main)


## Contributors
Thanks to Creator of this package [Jade](https://github.com/knisshoku), [uqlel](https://github.com/uqlel), [andressantamaria2003](https://github.com/andressantamaria2003), and [simonfrfr](https://github.com/simonfrfr).

## Notes
Thanks to Creator of this package [ttarvis](https://github.com/ttarvis) for writing [node-proxmox](https://github.com/ttarvis/node-proxmox)! Code was used for reference and function names are taken from it. Also thanks to [alo-is](https://github.com/alo-is) for writing another module also called [node-proxmox](https://github.com/alo-is/node-proxmox).
