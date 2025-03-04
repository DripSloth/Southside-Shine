
**Step 1: Configure External Collaboration in Azure Active Directory**

1. Log in to the **Azure portal** as a global administrator.
2. Navigate to **Azure Active Directory** → **External Identities** → **Cross-tenant access settings**.
3. Under **Default settings**, ensure the following are allowed:
    
    - **Inbound access:** Allow invitations and collaboration from the external tenant.
    - **Outbound access:** Allow your users to access the external tenant.
4. Click **Add organization**, enter the domain of the external tenant, and adjust the specific settings for collaboration (e.g., conditional access, trust relationships).
 
**Step 2: Invite Users from the Other Tenant**

1. Navigate to **Azure Active Directory** → **Users** → **New guest user**.
2. Select **Invite user** and enter the email address of the external user.
3. Assign the user to the appropriate **group** or **role** for permissions.
4. Click **Send invitation**. The external user will receive an email to accept the invitation.
 
**Step 3: Set Up Sharing in SharePoint Online and OneDrive**

1. Log in to the **Microsoft 365 Admin Center** and navigate to **SharePoint Admin Center**.
2. Under **Policies** → **Sharing**, enable:
    
    - **External sharing:** Allow sharing with users in specific domains (add the external tenant's domain).
3. Adjust library or folder permissions:
    
    - In the SharePoint site, go to the document library or folder.
    - Click **Share** and enter the external user's email. Grant appropriate access (e.g., view, edit).
 
**Step 4: Enable Guest Access in Microsoft Teams**

1. In the **Teams Admin Center**, go to **Org-wide settings** → **Guest access**.
2. Turn on **Allow guest access in Teams**.
3. Configure guest permissions:
    
    - Allow chat, calls, meetings, and file-sharing capabilities.
4. Invite external users to a team:
    
    - In Teams, click **Add member** to a team, enter the external user’s email, and send an invitation.
 
**Step 5: Configure Cross-Tenant Mail Flow (Optional)**  
For shared mail or calendar access:

1. In **Exchange Admin Center**, configure **Mail Flow** settings:
    
    - Create a new **Connector** to route mail between the tenants.
2. Allow cross-tenant calendar sharing:
    
    - In **Exchange Admin Center**, go to **Organization** → **Sharing**.
    - Add a sharing policy with the external tenant's domain.
 
**Step 6: Apply Security and Compliance Settings**

1. Enable conditional access for external users:
    
    - In **Azure Active Directory**, navigate to **Security** → **Conditional Access**.
    - Create a new policy to enforce multi-factor authentication (MFA) for external users.
2. Monitor access:
    
    - Use **Azure AD Sign-In Logs** to track external collaboration activities.
 
**Step 7: Test the Setup**

1. Invite a user from the external tenant and verify that:
    
    - They can access shared resources (SharePoint, Teams, etc.).
    - Communication (email, calendar sharing) works seamlessly.
2. Test file sharing, chat, and application access.