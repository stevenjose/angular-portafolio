# Upgrade Plan

This project is currently on Angular 10.2.5. Upgrading directly to the latest Angular version requires migrating each major version sequentially. Because the automated `ng update` process requires multiple steps, manual intervention is needed.

## Recommended steps
1. Upgrade to Angular 11:
   ```
   npm install -g @angular/cli@11
   ng update @angular/core@11 @angular/cli@11 --force
   ```
2. After verifying the application works, repeat the update for each major release:
   ```
   ng update @angular/core@12 @angular/cli@12 --force
   ng update @angular/core@13 @angular/cli@13 --force
   ng update @angular/core@14 @angular/cli@14 --force
   ...
   ```
3. Once on Angular 14 or later, components can be migrated to standalone by using the `standalone: true` flag and adjusting imports accordingly.

Due to the time-consuming nature of these updates, the changes have not been applied automatically.
