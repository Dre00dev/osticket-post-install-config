# osTicket Post Install Config
Create Departments, Roles, Agents, Users, SLAs

### Important Links:  
- [Create New Tickets](http://localhost/osTicket)  
- [Admin/Agent Login](http://localhost/osticket/scp/login.php)  

## Creating Departments and Roles  

### Departments vs. Roles  
- **Departments**: Containers that organize Agents.  
- **Roles**: Permissions defining what actions an Agent can perform.  

### Steps to Login as Admin  
1. Use the [Admin Login](http://localhost/osticket/scp/login.php) link.  
2. Enter your username/email and password.  
3. Ensure you are in the **Admin Panel** (if it says "Agent Panel" in the top-right, toggle to switch to Admin Panel).  

### Creating Departments  
1. Navigate to **Admin Panel** > `Agents` > `Departments` > `Add New Department`  
2. **Name**: System Administrators  
3. Click `Create Department`  

### Creating Roles  
1. Navigate to **Agents** > `Roles` > `Add New Role`  
2. **Name**: GlobalAdminAccess  
3. Click the `Permissions` tab and check all boxes under:  
   - **Tickets**  
   - **Tasks**  
   - **Knowledgebase**  
4. Click `Add Role`  

## Creating Agents and Teams  

### Creating Agents  
1. Navigate to **Agents** > `Add New Agents`  
2. **Name**: Pat Henshaw  
3. **Email**: `phenshaw@helpdesk.com`  
4. **Username**: `phenshaw`  
5. Click `Set Password`, then:  
   - Uncheck **Send the Agent a Password Reset Email**  
   - Set a password manually  
   - Uncheck **Require Password Change at Next Login** _(not recommended in real-world scenarios)_  
6. Click `Set`  
7. Navigate to **Access tab**:  
   - **Department**: System Administrators  
   - **Role**: GlobalAdminAccess  
   - **Extended Access**:  
     - Select **Support** > `Add` > `GlobalAdminAccess`  

**Follow the same steps** to create another Agent named **Jerry Moore**.  

### Creating Teams  
1. Navigate to **Agents** > `Teams` > `Add New Team`  
2. **Name**: Level II Support _(since Level I exists by default)_  
3. Navigate to the `Members` tab:  
   - Add **Pat Henshaw** and your **Admin account**  
4. Click `Create Team`  

To modify **Level I Support**:  
1. Navigate to **Teams** > `Level I Support`  
2. Add **Jerry Moore** as a member  

## Creating Help Topics, SLAs, and Users  

### Creating Help Topics  
1. Navigate to **Manage** > `Help Topics` > `Add New Help Topic`  
2. **Topic**: Business Critical Failure  
3. Repeat for additional topics:  
   - **Personal Computer Issues**  
   - **Password Reset**  

### Creating SLAs  
1. Navigate to **Manage** > `SLA` > `Add New SLA Plan`  
2. **Name**: Priority 1  
3. **Grace Period**: 1  
4. **Schedule**: 24/7  
5. Click `Add Plan`  
6. Repeat for **Priority 2** and **Priority 3**  

### Creating Users  
1. Ensure you are in the **Agent Panel**  
2. Navigate to **Users** > `Add New User`  
3. **Email Address**: `hjones@helpdesk.com`  
4. **Full Name**: Henry Jones  
5. Click `Add User`  
6. Repeat for two more users as shown in the User Directory  

### Allow Anyone to Create Tickets  
1. Navigate to **Settings** > `User Settings`  
2. Uncheck:  
   - **Registration Required**: Require registration and login to create tickets  

---

This completes the setup process for osTicket! 🚀
