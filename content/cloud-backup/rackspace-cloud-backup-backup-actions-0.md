---
node_id: 2040
title: Cloud Backup actions
type: article
created_date: '2012-08-22'
created_by: David Hendler
last_modified_date: '2016-01-21'
last_modified_by: Margaret Eker
product: Cloud Backup
product_url: cloud-backup
---

### Previous section

[View backup
information with Cloud Backup](/how-to/rackspace-cloud-backup-view-backup-information)

### How to Use Backup Actions

You can perform several actions with a single backup. This page
describes those actions.

You can access the **Backup Actions** menu in two ways:

-   From the gear icon next to the backup name on the Configured
    Backups page.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%204.20.11%20PM.png" width="479" height="292" />

-   From the **Actions** menu at the top of the details page for a
    configured backup.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%204.18.36%20PM.png" width="552" height="219" />

From the **Backup Actions** menu, you can perform the following actions:

-   Perform Backup
-   Restore Backup
-   [Configure Backup](#configurebackup)
-   [Configure Files](#configurefiles)
-   [Disable Backup](#disablebackup)
-   [Delete Backup](#deletebackup)

### Perform Backup

When you select **Perform Backup**, you trigger a manual backup on your
system, based on the configurations that are currently set for that
configured backup.
If you are looking at the **Configuration Details** page, the backup
progress bar is displayed until the backup is completed.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%204.29.20%20PM.png" width="666" height="101" />

### Restore Backup

Use the **Restore Backup** action to restore a backup.

1.  From the **Backup Actions** menu, select the **Restore Backup.**

2.  On the first page of the Restore a Backup wizard, select the
    **Backup Date** to restore from, and then click **Next Step**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%204.34.50%20PM.png" width="491" height="264" />

3.  On the next page, select the destination system, and then click
    **Next Step**.

-   You can limit the list of systems by using the search box.
-   You can restore your backup to the system that was backed up, or to
    another system.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%204.42.12%20PM.png" width="498" height="282" />

4.  On the next page, select the folders and files to restore.

-   On the **Browse Files & Folders** tab, select the check boxes of the
    files and folders that you want to restore.
    You can move through your folders by clicking **Up** or an
    individual folder name at top of the file or folder list.
-   After you have selected your files, you can confirm your selection
    by clicking the **Selected & Excluded Items** tab.
    The files included in the restore and specifically excluded
    are listed.
-   When you are satisfied with your selection, click **Next Step**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%204.53.59%20PM.png" width="497" height="337" />

5.  On the next page, select the destination folder.

           You can choose to restore the files to their original folder
or to restore to a selected restore destination.
           You can also select whether to overwrite files with the same
name. Then, click **Next** **Step**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%205.13.30%20PM.png" width="500" height="274" />

6.  Confirm your restore settings and then click **Start Restore**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%205.20.03%20PM.png" width="503" height="287" />

The **Activity** page is displayed when the restore is complete.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-15%20at%205.22.45%20PM.png" width="608" height="140" />

### Configure Backup

You can change the name, recurrence, and notifications for your backup
job. Select **Configure Backup** from the
**Backup Actions** menu to view these settings.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-16%20at%201.23.19%20PM.png" width="528" height="593" />

1.  Enter a new name for your backup job, and under **Schedule**, select
    how often you want to run the backup. All times are Central Time.

**Note**: You can schedule your backups for as often as you expect your
files to change. Cloud Backup uses block-level de-duplication, which
means only those parts of a file that have changed are saved. In this
way, a unique piece of data is saved only once, which maximizes the
effectiveness of the backup, while minimizing your storage overhead.
Another benefit is that by using this method, you can retrieve previous
versions of files, up to the limits specified by the customer-defined
retention settings.

To save additional overhead, Cloud Backup might compress the files if it
reduces the size of the block. You can expect compression rates
equivalent to those of gzip. You should not try to manually compress or
encrypt your data before running backups; if you do, deduplication will
not work, and  you will create larger backups than you need. If you want
to encrypt your backups, see the section on [Encrypting your
System](/how-to/rackspace-cloud-backup-system-actions#encryptsystem) in
this guide.

For advanced Linux users, if you create tarballs with gzip that will get
backed up, be sure to use gzip's ` --rsyncable` option, which this Cloud
Backup to deduplication those files as well.


2.  Select how long you want to keep your backups: 30 days, 60 days, or
    indefinitely.

3.  Under **Notifications**, enter the email address where you want to
    receive notifications of failed backups. You can also elect to have
    emails sent for successful backups.

4.  When you are satisfied with your settings, click **Next Step**.

5.  On the next page, select the folders and files for the backup, along
    with any files you want
    to exclude. Then click **Next Step**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-16%20at%201.37.49%20PM.png" width="527" height="363" />

6.  On the next page, review your backup configuration settings. If the
    settings are correct, click **Save**. Otherwise, click **Back** to
    make changes.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-16%20at%201.46.18%20PM.png" width="533" height="315" />

### Configure Files

You can change the files and folders that are saved in your backup.
Click **Configure Files** from the **Backup Actions** menu to view these
settings.

1.  On the **Browse Files & Folders** tab, select the the folders and
    files by clicking the folder name to view which files are inside.
    Select the check boxes of the files and folders that you want to
    back up.

2.  Confirm your selection by clicking the **Selected & Excluded
    Items** tab. The files included, as well as those specifically
    excluded, are listed.

3.  Click **Next Step**.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-16%20at%201.37.49%20PM.png" width="537" height="370" />

4. Confirm the settings on the next page and click **Save** to save
   your file configuration.

### Disable Backup

You can prevent a backup from running by selecting **Disable Backup**
from the **Backup Actions** menu.

<img src="https://8026b2e3760e2433679c-fffceaebb8c6ee053c935e8915a3fbe7.ssl.cf2.rackcdn.com/field/image/Screen%20Shot%202015-10-16%20at%202.36.44%20PM.png" width="564" height="348" />

When you disable a backup, the following actions occur:

-   The backup status changesfrom to **Disabled**.
-   The **Perform Backup** button becomes unavailable.

To re-enable your backup, from the **Backup Actions** menu, select
**Enable Backup**. Your backup returns to **Active** status with all its
previous settings.

### Delete Backup

You can delete your backup by selecting **Delete Backup** from the
**Backup Actions** menu.

Confirm that you want to delete the backup.

After a backup is deleted, it cannot be recovered.

### Next steps

[Cloud Backup System
actions](/how-to/rackspace-cloud-backup-system-actions)
