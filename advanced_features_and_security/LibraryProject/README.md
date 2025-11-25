# Django Permissions and Groups Setup

## Custom Permissions
The Book model includes custom permissions:
- `can_view_book`: View book details
- `can_create_book`: Create new books
- `can_edit_book`: Edit existing books
- `can_delete_book`: Delete books

## Groups Configuration
Create these groups in Django Admin:
- **Viewers**: Assign `can_view_book` permission
- **Editors**: Assign `can_view_book`, `can_create_book`, `can_edit_book` permissions
- **Admins**: Assign all permissions

## Views with Permission Checks
All CRUD views use `@permission_required` decorators to enforce access control.

## Testing
1. Create test users in Django Admin
2. Assign users to different groups
3. Test access to views with different user roles