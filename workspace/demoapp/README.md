# ace-log4j-demo-issue


mqsicreatebroker ACENODE -q ACEQM

runmqsc ACEQM

define qlocal (Q1.BOQ)
define qlocal (Q1) BOQNAME(Q1.BOQ) BOTHRESH(3)

define qlocal (Q2.BOQ)
define qlocal (Q2) BOQNAME(Q2.BOQ) BOTHRESH(3)


mqsiapplybaroverride -b D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin11.bar -p D:\git\github\ace-log4j-demo-issue\workspace\demoapp\demoapp.properties -o D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin11-output.bar -r

mqsideploy ACENODE -e acedemois -a D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin11-output.bar -m

mqsireadbar -b demoapp.bar -r
BIP1052I: Reading Bar file using runtime mqsireadbar...
demoapp.bar:
  demoapp.appzip (6/03/23 12:54 AM):
    application.descriptor (6/03/23 12:54 AM):
    brokerlog-log4j.xml (6/03/23 12:54 AM):
    brokerlog-log4j2.xml (6/03/23 12:54 AM):
    demoflow.cmf (6/03/23 12:54 AM):
    Deployment descriptor:
      startMode
      demoflow#additionalInstances
      demoflow#commitCount
      demoflow#commitInterval
      demoflow#coordinatedTransaction
      demoflow#consumerPolicySet
      demoflow#providerPolicySet
      demoflow#consumerPolicySetBindings
      demoflow#providerPolicySetBindings
      demoflow#securityProfileName
      demoflow#monitoringProfile
      demoflow#startMode
      demoflow#startInstancesWhenFlowStarts
      demoflow#maximumRateMsgsPerSec
      demoflow#wlmPolicy
      demoflow#notificationThresholdMsgsPerSec
      demoflow#processingTimeoutSec
      demoflow#processingTimeoutAction
      demoflow#Log Message.log4jConfigFile = brokerlog.xml
      demoflow#Log Message.logLevel = INFO
      demoflow#Log Message.logText = My Message is $/$
      demoflow#Log Message.loggerName = FILE
      demoflow#MQ Input.SSLCertificateLabel
      demoflow#MQ Input.SSLCipherSpec
      demoflow#MQ Input.SSLPeerName
      demoflow#MQ Input.additionalInstances
      demoflow#MQ Input.channelName
      demoflow#MQ Input.componentLevel
      demoflow#MQ Input.connection
      demoflow#MQ Input.destinationQueueManagerName
      demoflow#MQ Input.listenerPortNumber
      demoflow#MQ Input.policyUrl
      demoflow#MQ Input.queueManagerHostname
      demoflow#MQ Input.queueName = Q1
      demoflow#MQ Input.resetBrowseTimeout
      demoflow#MQ Input.securityIdentity
      demoflow#MQ Input.securityProfileName
      demoflow#MQ Input.serializationToken
      demoflow#MQ Input.topicProperty
      demoflow#MQ Input.useSSL
      demoflow#MQ Input.validateMaster
      demoflow#MQ Output.AddRequestToGroup
      demoflow#MQ Output.GroupRequestFolderName
      demoflow#MQ Output.GroupRequestTimeout
      demoflow#MQ Output.SSLCertificateLabel
      demoflow#MQ Output.SSLCipherSpec
      demoflow#MQ Output.SSLPeerName
      demoflow#MQ Output.channelName
      demoflow#MQ Output.connection
      demoflow#MQ Output.destinationQueueManagerName
      demoflow#MQ Output.listenerPortNumber
      demoflow#MQ Output.policyUrl
      demoflow#MQ Output.queueManagerHostname
      demoflow#MQ Output.queueManagerName
      demoflow#MQ Output.queueName = Q2
      demoflow#MQ Output.replyToQ
      demoflow#MQ Output.replyToQMgr
      demoflow#MQ Output.securityIdentity
      demoflow#MQ Output.securityProfileName
      demoflow#MQ Output.useSSL
      demoflow#MQ Output.validateMaster

BIP8071I: Successful command completion.

D:\git\github\ace-log4j-demo-issue\workspace\BARfiles>mqsireadbar -b D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin11-output.bar -r
BIP1052I: Reading Bar file using runtime mqsireadbar...
D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin11-output.bar:
  demoapp.appzip (6/03/23 9:46 AM):
    application.descriptor (6/03/23 9:46 AM):
    brokerlog-log4j.xml (6/03/23 9:46 AM):
    brokerlog-log4j2.xml (6/03/23 9:46 AM):
    demoflow.cmf (6/03/23 9:46 AM):
    Deployment descriptor:
      startMode
      demoflow#additionalInstances
      demoflow#commitCount
      demoflow#commitInterval
      demoflow#coordinatedTransaction
      demoflow#consumerPolicySet
      demoflow#providerPolicySet
      demoflow#consumerPolicySetBindings
      demoflow#providerPolicySetBindings
      demoflow#securityProfileName
      demoflow#monitoringProfile
      demoflow#startMode
      demoflow#startInstancesWhenFlowStarts
      demoflow#maximumRateMsgsPerSec
      demoflow#wlmPolicy
      demoflow#notificationThresholdMsgsPerSec
      demoflow#processingTimeoutSec
      demoflow#processingTimeoutAction
      demoflow#Log Message.log4jConfigFile = D:\git\github\ace-log4j-demo-issue\workspace\demoapp\demoapp.properties
      demoflow#Log Message.logLevel = INFO
      demoflow#Log Message.logText = My Message is $/$
      demoflow#Log Message.loggerName = FILE
      demoflow#MQ Input.SSLCertificateLabel
      demoflow#MQ Input.SSLCipherSpec
      demoflow#MQ Input.SSLPeerName
      demoflow#MQ Input.additionalInstances
      demoflow#MQ Input.channelName
      demoflow#MQ Input.componentLevel
      demoflow#MQ Input.connection
      demoflow#MQ Input.destinationQueueManagerName
      demoflow#MQ Input.listenerPortNumber
      demoflow#MQ Input.policyUrl
      demoflow#MQ Input.queueManagerHostname
      demoflow#MQ Input.queueName = Q1
      demoflow#MQ Input.resetBrowseTimeout
      demoflow#MQ Input.securityIdentity
      demoflow#MQ Input.securityProfileName
      demoflow#MQ Input.serializationToken
      demoflow#MQ Input.topicProperty
      demoflow#MQ Input.useSSL
      demoflow#MQ Input.validateMaster
      demoflow#MQ Output.AddRequestToGroup
      demoflow#MQ Output.GroupRequestFolderName
      demoflow#MQ Output.GroupRequestTimeout
      demoflow#MQ Output.SSLCertificateLabel
      demoflow#MQ Output.SSLCipherSpec
      demoflow#MQ Output.SSLPeerName
      demoflow#MQ Output.channelName
      demoflow#MQ Output.connection
      demoflow#MQ Output.destinationQueueManagerName
      demoflow#MQ Output.listenerPortNumber
      demoflow#MQ Output.policyUrl
      demoflow#MQ Output.queueManagerHostname
      demoflow#MQ Output.queueManagerName
      demoflow#MQ Output.queueName = Q2
      demoflow#MQ Output.replyToQ
      demoflow#MQ Output.replyToQMgr
      demoflow#MQ Output.securityIdentity
      demoflow#MQ Output.securityProfileName
      demoflow#MQ Output.useSSL
      demoflow#MQ Output.validateMaster

BIP8071I: Successful command completion.

D:\IBM\ACE\12.0.7.0>mqsireadbar -b D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin20.bar -r
BIP1052I: Reading Bar file using runtime mqsireadbar...
D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin20.bar:
  demoapp.appzip (6/03/23 10:39 AM):
    application.descriptor (6/03/23 10:39 AM):
    brokerlog-log4j.xml (6/03/23 10:39 AM):
    brokerlog-log4j2.xml (6/03/23 10:39 AM):
    demoflow.cmf (6/03/23 10:39 AM):
    Deployment descriptor:
      startMode
      demoflow#additionalInstances
      demoflow#commitCount
      demoflow#commitInterval
      demoflow#coordinatedTransaction
      demoflow#consumerPolicySet
      demoflow#providerPolicySet
      demoflow#consumerPolicySetBindings
      demoflow#providerPolicySetBindings
      demoflow#securityProfileName
      demoflow#monitoringProfile
      demoflow#startMode
      demoflow#startInstancesWhenFlowStarts
      demoflow#maximumRateMsgsPerSec
      demoflow#wlmPolicy
      demoflow#notificationThresholdMsgsPerSec
      demoflow#processingTimeoutSec
      demoflow#processingTimeoutAction
      demoflow#MQ Input.SSLCertificateLabel
      demoflow#MQ Input.SSLCipherSpec
      demoflow#MQ Input.SSLPeerName
      demoflow#MQ Input.additionalInstances
      demoflow#MQ Input.channelName
      demoflow#MQ Input.componentLevel
      demoflow#MQ Input.connection
      demoflow#MQ Input.destinationQueueManagerName
      demoflow#MQ Input.listenerPortNumber
      demoflow#MQ Input.policyUrl
      demoflow#MQ Input.queueManagerHostname
      demoflow#MQ Input.queueName = Q1
      demoflow#MQ Input.resetBrowseTimeout
      demoflow#MQ Input.securityIdentity
      demoflow#MQ Input.securityProfileName
      demoflow#MQ Input.serializationToken
      demoflow#MQ Input.topicProperty
      demoflow#MQ Input.useSSL
      demoflow#MQ Input.validateMaster
      demoflow#MQ Output.AddRequestToGroup
      demoflow#MQ Output.GroupRequestFolderName
      demoflow#MQ Output.GroupRequestTimeout
      demoflow#MQ Output.SSLCertificateLabel
      demoflow#MQ Output.SSLCipherSpec
      demoflow#MQ Output.SSLPeerName
      demoflow#MQ Output.channelName
      demoflow#MQ Output.connection
      demoflow#MQ Output.destinationQueueManagerName
      demoflow#MQ Output.listenerPortNumber
      demoflow#MQ Output.policyUrl
      demoflow#MQ Output.queueManagerHostname
      demoflow#MQ Output.queueManagerName
      demoflow#MQ Output.queueName = Q2
      demoflow#MQ Output.replyToQ
      demoflow#MQ Output.replyToQMgr
      demoflow#MQ Output.securityIdentity
      demoflow#MQ Output.securityProfileName
      demoflow#MQ Output.useSSL
      demoflow#MQ Output.validateMaster

BIP8071I: Successful command completion.


mqsiapplybaroverride -b D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin20.bar -p D:\git\github\ace-log4j-demo-issue\workspace\demoapp\demoapp-logging-plugin20.properties -o D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin20-output.bar -r

mqsideploy ACENODE -e acedemois -a D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin20-output.bar -m

mqsireadbar -b D:\git\github\ace-log4j-demo-issue\workspace\BARfiles\demoapp-logging-plugin20-output.bar -r