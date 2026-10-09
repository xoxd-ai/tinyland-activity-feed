# tinyland-activity-feed (retired)

This repository is retired and archived. Do not add new consumers.

The activity feed was merged into
[`xoxd-ai/tinyland-content`](https://github.com/xoxd-ai/tinyland-content)
on 2026-10-08 (U2 package wave, rulings RU2 and RU7). The code and tests moved
unchanged to `src/activity-feed/` there.

## Replacement

- Bazel module: `tummycrypt_tinyland_content` 0.5.0 or later
  (`bazel_dep(name = "tummycrypt_tinyland_content", version = "0.5.0")`).
  Drop `bazel_dep(name = "tummycrypt_tinyland_activity_feed", ...)`, its
  overrides and its `npm_link_package`.
- Imports: replace `@tummycrypt/tinyland-activity-feed` with
  `@tummycrypt/tinyland-content/activity-feed`. The names are the same
  (`configure`, `getConfig`, `resetConfig`, `getRecentActivityServer`,
  `getActivityByTypeServer`, `getActivityByCategoryServer`,
  `getActivityByTagServer`, `searchActivityServer` and the item types).
- Or import from the `@tummycrypt/tinyland-content` root, where the config
  helpers are named `configureActivityFeed`, `getActivityFeedConfig` and
  `resetActivityFeedConfig`.

## Existing versions

`tummycrypt_tinyland_activity_feed` 0.2.0 stays in
[`xoxd-ai/bazel-registry`](https://github.com/xoxd-ai/bazel-registry) and
still resolves; its metadata is marked deprecated. Nothing was yanked or
unpublished. The npmjs versions of `@tummycrypt/tinyland-activity-feed`
(0.1.0 to 0.2.2) stay published and should not be used; they are marked
deprecated (RU8) once an npm login is available.
