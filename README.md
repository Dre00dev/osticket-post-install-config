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
![osticketsignin1](https://github.com/user-attachments/assets/ab3ad7a7-b057-40e0-b2a0-7c835682f411)

### Creating Departments  
1. Navigate to **Admin Panel** > `Agents` > `Departments` > `Add New Department`  
2. **Name**: System Administrators  
3. Click `Create Department`  
![osticketdept2](https://github.com/user-attachments/assets/c31aab49-669f-4006-b5f9-929b963cea61)

### Creating Roles  
1. Navigate to **Agents** > `Roles` > `Add New Role`  
2. **Name**: GlobalAdminAccess  
3. Click the `Permissions` tab and check all boxes under:  
   - **Tickets**  
   - **Tasks**  
   - **Knowledgebase**  
4. Click `Add Role`  
![addroleosticket3](https://github.com/user-attachments/assets/9f8fd426-e4a2-4486-a4de-b3cfa1fbf1f0)

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
![addagent4](https://github.com/user-attachments/assets/d8ce728f-255c-4755-a641-24073272953b)
![addagent5](https://github.com/user-attachments/assets/f5dc9e1f-2072-4b66-a0ed-d08d81b98b1b)
![agentlist6](https://github.com/user-attachments/assets/cc0416b0-6fec-424a-81fa-837ae3d9d4bd)

### Creating Teams  
1. Navigate to **Agents** > `Teams` > `Add New Team`  
2. **Name**: Level II Support _(since Level I exists by default)_  
3. Navigate to the `Members` tab:  
   - Add **Pat Henshaw** and your **Admin account**  
4. Click `Create Team`  
![level2support7](https://github.com/user-attachments/assets/e2129142-caef-4e24-b74e-27d1ab587e7a)

To modify **Level I Support**:  
1. Navigate to **Teams** > `Level I Support`  
2. Add **Jerry Moore** as a member  
![level1support8](https://github.com/user-attachments/assets/05b6d3b8-c8aa-463d-ab62-e70bd1ca7d53)

## Creating Help Topics, SLAs, and Users  

### Creating Help Topics  
1. Navigate to **Manage** > `Help Topics` > `Add New Help Topic`  
2. **Topic**: Business Critical Failure  
3. Repeat for additional topics:  
   - **Personal Computer Issues**  
   - **Password Reset**  
![addnewhelptopic9](https://github.com/user-attachments/assets/d93c822a-d4b1-48ce-bd77-65ce1e005411)
![helptopiclist10](https://github.com/user-attachments/assets/c6045d93-d231-4451-bb2e-b18b0ef62846)

### Creating SLAs  
1. Navigate to **Manage** > `SLA` > `Add New SLA Plan`  
2. **Name**: Priority 1  
3. **Grace Period**: 1  
4. **Schedule**: 24/7  
5. Click `Add Plan`  
6. Repeat for **Priority 2** and **Priority 3**  
![slaplan11](https://github.com/user-attachments/assets/c608e57c-4b0a-4979-bc50-e6acba0f7ece)
![slalist 12](https://github.com/user-attachments/assets/4576dc26-bf8c-4135-b2b9-d6444173f340)

### Creating Users  
1. Ensure you are in the **Agent Panel**  
2. Navigate to **Users** > `Add New User`  
3. **Email Address**: `hjones@helpdesk.com`  
4. **Full Name**: Henry Jones  
5. Click `Add User`  
6. Repeat for two more users as shown in the User Directory  
![user list 13](https://github.com/user-attachments/assets/97731a6e-a99a-431c-85a5-ce5f2c0dd637)

### Allow Anyone to Create Tickets  
1. Navigate to **Settings** > `User Settings`  
2. Uncheck:  
   - **Registration Required**: Require registration and login to create tickets  

---

This completes the setup process for osTicket! 🚀
