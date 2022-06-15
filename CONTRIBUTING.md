# Conventional Commits 1.0.0


So in short the standard commit style i will be using is:
```
<type>(<File Or Function>): <Message>
<type> <Github Issue> // This is optional
```
The types that i will be using are:
```
feat:     A new feature
fix:      A bug fix
docs:     Documentation only changes
style:    Changes that do not affect the meaning of the code (white-space, for matting, missing semi-colons, etc)
refactor: A code change that neither fixes a bug nor adds a feature
perf:     A code change that improves performance
test:     Adding missing tests or correcting existing tests
build:    Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
  ci:       Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
```

## Summary
The Conventional Commits specification is a lightweight convention on top of commit messages. It provides an easy set of rules for creating an explicit commit history; which makes it easier to write automated tools on top of. This convention dovetails with SemVer, by describing the features, fixes, and breaking changes made in commit messages

The commit message should be structured as follows:
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

<p>
The commit contains the following structural elements, to communicate intent to the
consumers of your library:</p>

<ol>
  <li>
    <strong>fix:</strong> a commit of the <em>type</em> <code>fix</code> patches
    a bug in your codebase 
  </li>
  <li>
    <strong>feat:</strong> a commit of the <em>type</em>
    <code>feat</code> introduces a new feature to the codebase
  </li>
  <li>
    <strong>BREAKING CHANGE:</strong> a commit that has a footer
    <code>BREAKING CHANGE:</code>, or appends a <code>!</code> after the
    type/scope, introduces a breaking API change.A BREAKING CHANGE can be part of commits of any <em>type</em>.
  </li>
  <li>
    <em>types</em> other than <code>fix:</code> and <code>feat:</code> are
    allowed, Examples are  <code>build:</code>, <code>chore:</code>, <code>ci:</code>,
    <code>docs:</code>, <code>style:</code>, <code>refactor:</code>,
    <code>perf:</code>, <code>test:</code>, and others.
  </li>
  <li>
    <em>footers</em> other than
    <code>BREAKING CHANGE: &lt;description&gt;</code> may be provided and follow
    a convention similar to
    <a href="https://git-scm.com/docs/git-interpret-trailers"
      >git trailer format</a
    >.
  </li>
</ol>


## Examples
### Commit message with description and breaking change footer
```
feat: allow provided config object to extend other configs

BREAKING CHANGE: `extends` key in config file is now used for extending other config files
```

### Commit message with ! to draw attention to breaking change

```
feat!: send an email to the customer when a product is shipped
```

### Commit message with scope and ! to draw attention to breaking change

```
feat(api)!: send an email to the customer when a product is shipped
```

### Commit message with both ! and BREAKING CHANGE footer

```
chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```
### Commit message with no body
```
docs: correct spelling of CHANGELOG
```
### Commit message with scope
```
feat(lang): add Polish language
```
### Commit message with multi-paragraph body and multiple footers

```
fix: prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```
