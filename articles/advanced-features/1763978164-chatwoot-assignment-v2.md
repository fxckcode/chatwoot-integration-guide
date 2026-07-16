# Advanced Assignment Policies

## **Overview**

The advanced assignment introduces a comprehensive policy-based conversation assignment system. This provides centralized management, advanced algorithms, and enterprise-grade capacity controls.

## Feature Availability

* **Open Source**: Assignment policies with round-robin algorithm

* **Enterprise and Business**: All OSS features plus balanced assignment and agent capacity management

## **Core Concepts**

### **Assignment Policies**

Assignment policies are centralized rules that control how conversations are automatically assigned to agents. Each policy defines:

* **Assignment Order**: How agents are selected (round-robin or balanced)

* **Conversation Priority**: Which conversations get assigned first

* **Fair Distribution**: Rate limiting to prevent agent overload

### **Agent Capacity Policies (Enterprise)**

Capacity policies set conversation limits per agent with inbox-specific granularity and advanced filtering rules.

## **Assignment Policies**

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT1NyekFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f24c68492616afdb348599d34c025ad079d55e96/image.png?cw_image_width=698px)

### **Creating Assignment Policies**

1. Navigate to **Settings → Agent assignment → Assignment policy**

2. Click **Create Assignment Policy**

3. Configure the following:

#### **Basic Configuration**

* **Name**: Unique policy identifier

* **Description**: Optional policy description

* **Enabled**: Toggle policy activation

#### **Assignment Settings**

* **Assignment Order**:

  * `Round Robin`: Cycles through available agents sequentially (OSS & Enterprise)

  * `Balanced`: Distributes based on current workload, equal assignment (Enterprise only)

* **Conversation Priority**:

  * `Earliest Created`: Assigns oldest conversations first

  * `Longest Waiting`: Prioritizes conversations with longest wait times

* **Fair Distribution:**

  * **Limit**: Maximum conversations per agent within time window (default: 100)

  * **Window**: Time period in seconds for rate limiting (default: 3600)

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR0d0ekFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c2dbb570a90cc372f327b16aa52aead043338950/image.png?cw_image_width=717px)

### **Linking Policies to Inboxes**

1. Go to **Settings → Agent Assignment**

2. Edit a policy.

3. Add an Inbox.

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRnl4ekFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--6349b4917312c54c06d67da4c6d12586604939eb/image.png?cw_image_width=661px)

## **Agent Capacity Management (Enterprise)**

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRUd5ekFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c27e1f7e0057230c1f6e9b619368ef044b84902e/image.png?cw_image_width=721px)

### **Creating Capacity Policies**

1. Navigate to **Settings → Assignment Policy → Capacity**

2. Click **Create Capacity Policy**

3. Configure:

   1. **Basic Settings**

      1. **Name**: Policy identifier

      2. **Description**: Optional description

   2. **Inbox Capacity Limits**

      1. For each inbox, set:

      2. **Conversation Limit**: Maximum open conversations per agent

   3. **Exclusion Rules (JSON Configuration)**

      1. **Excluded Labels**: Conversations with these labels won't be auto-assigned

      2. **Age Threshold**: Exclude conversations older than specified hours

   ![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCR2kxekFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--2f44296bac64a47e1d7d44d9d82f8ab0817ba9e5/image.png?cw_image_width=680px)

### **Assigning Capacity Policies to Agents**

1. Go to **Assignment Policy → Agent Capacity Policy**

2. Select an Agent Capacity Policy

3. Add Inbox capacity limits

4. Assign agents to the policy

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCRHEzekFJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--f1e66032d115014b91870bd36de06c331be999ff/image.png?cw_image_width=726px)

## **Assignment Algorithms**

### **Round Robin (OSS & Enterprise)**

Cycles through available agents sequentially, ensuring equal distribution over time.

### **Balanced Assignment (Enterprise)**

Intelligently distributes conversations based on:

* Current agent workload

* Equal assignment

## **Troubleshooting**

### **Common Issues**

#### **Conversations Not Being Assigned**

* Verify assignment policy is enabled and linked to inbox

* Check if agents are available and online

* Ensure agents haven't reached capacity limits (Enterprise)

* Verify exclusion rules aren't filtering out conversations

#### **Uneven Distribution**

* Review fair distribution settings

* Consider switching to balanced assignment (Enterprise)

* Check agent availability patterns

### **Debugging Steps**

1. Check assignment policy configuration

2. Verify inbox-policy linkage

3. Review agent capacity settings (Enterprise)

4. Monitor assignment service logs

5. Validate agent availability status

Assignment V2 provides a robust, scalable solution for conversation management that grows with your organization's needs while maintaining optimal agent workload distributio
