# Displaying Dotkernel API endpoints using dot-cli

## Usage

Run the following command in your application’s root directory:

```shell
php ./bin/cli.php route:list
```

The command runs through all routes and extracts endpoint information in realtime.
The output should be similar to the following:

```text
+-------------------- 37 Routes ------+-------------------------------------+
| Request method | Route name                          | Route path                          |
+----------------+-------------------------------------+-------------------------------------+
| GET            | app::view-index                     | /                                   |
| GET            | admin::list-admin                   | /admin                              |
| POST           | admin::create-admin                 | /admin                              |
| GET            | admin::view-account                 | /admin/account                      |
| PATCH          | admin::update-account               | /admin/account                      |
| GET            | admin::list-role                    | /admin/role                         |
| GET            | admin::view-role                    | /admin/role/{uuid}                  |
| DELETE         | admin::delete-admin                 | /admin/{uuid}                       |
| GET            | admin::view-admin                   | /admin/{uuid}                       |
| PATCH          | admin::update-admin                 | /admin/{uuid}                       |
| POST           | app::create-error-report            | /error-report                       |
| POST           | security::token                     | /security/token                     |
| GET            | user::list-user                     | /user                               |
| POST           | user::create-user                   | /user                               |
| DELETE         | user::delete-account                | /user/account                       |
| GET            | user::view-account                  | /user/account                       |
| PATCH          | user::update-account                | /user/account                       |
| POST           | user::create-account                | /user/account                       |
| POST           | user::request-activate-account      | /user/account/activate              |
| PATCH          | user::activate-account              | /user/account/activate/{hash}       |
| DELETE         | user::delete-account-avatar         | /user/account/avatar                |
| GET            | user::view-account-avatar           | /user/account/avatar                |
| POST           | user::create-account-avatar         | /user/account/avatar                |
| POST           | user::recover-account               | /user/account/recover               |
| POST           | user::create-account-reset-password | /user/account/reset-password        |
| GET            | user::check-account-reset-password  | /user/account/reset-password/{hash} |
| PATCH          | user::update-account-reset-password | /user/account/reset-password/{hash} |
| GET            | user::list-role                     | /user/role                          |
| GET            | user::view-role                     | /user/role/{uuid}                   |
| DELETE         | user::delete-user                   | /user/{uuid}                        |
| GET            | user::view-user                     | /user/{uuid}                        |
| PATCH          | user::update-user                   | /user/{uuid}                        |
| PATCH          | user::activate-user                 | /user/{uuid}/activate               |
| DELETE         | user::delete-user-avatar            | /user/{uuid}/avatar                 |
| GET            | user::view-user-avatar              | /user/{uuid}/avatar                 |
| POST           | user::create-user-avatar            | /user/{uuid}/avatar                 |
| PATCH          | user::deactivate-user               | /user/{uuid}/deactivate             |
+------+----------------+-------------------------------------+-------------------------------------+

```

## Filtering results

The following filters can be applied when displaying the routes list:

* Filter routes by name, using: `-i|--name[=NAME]`
* Filter routes by path, using: `-p|--path[=PATH]`
* Filter routes by method, using: `-m|--method[=METHOD]`

The filters are case-insensitive and can be combined.

Get more help by running this command:

```shell
php ./bin/cli.php route:list --help
```
