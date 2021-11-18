<!--

  DO NOT EDIT.

  This markdown file was autogenerated using a mixture of the following files as the source of truth for its data:
  - ../../src/rules/no-output-rename.ts
  - ../../tests/rules/no-output-rename/cases.ts

  In order to update this file, it is therefore those files which need to be updated, as well as potentially the generator script:
  - ../../../../tools/scripts/generate-rule-docs.ts

-->

<br>

# `@angular-eslint/no-output-rename`

Ensures that output bindings are not aliased

- Type: suggestion
- 🔧 Supports autofix (`--fix`)

- 💡 Provides suggestions on how to fix issues (https://eslint.org/docs/developer-guide/working-with-rules#providing-suggestions)

<br>

## Rule Options

The rule does not have any configuration options.

<br>

## Usage Examples

> The following examples are generated automatically from the actual unit tests within the plugin, so you can be assured that their behavior is accurate based on the current commit.

<br>

<details>
<summary>❌ - Toggle examples of <strong>incorrect</strong> code for this rule</summary>

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Component({
  outputs: ['a: b']
            ~~~~~~
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  inputs: ['abort'],
  'outputs': [boundary, `test: copy`],
                        ~~~~~~~~~~~~
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Component({
  ['outputs']: ['orientation: orientation'],
                ~~~~~~~~~~~~~~~~~~~~~~~~~~
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  [`outputs`]: ['orientation: orientation'],
                ~~~~~~~~~~~~~~~~~~~~~~~~~~
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Component()
class Test {
  @Custom() @Output(`change`) _change = getOutput();
                    ~~~~~~~~
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive()
class Test {
  @Output('change') change = (this.subject$ as Subject<{blur: boolean}>).pipe();
          ~~~~~~~~
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  selector: 'foo'
})
class Test {
  @Output('fooColor') colors: string;
          ~~~~~~~~~~
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Component({
  'selector': 'foo'
})
class Test {
  @Output('foocolor') color: string;
          ~~~~~~~~~~
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  selector: 'kebab-case',
})
class Test {}

@Injectable()
class Test {
  @Output('kebab-case') blur = this.getOutput();
          ~~~~~~~~~~~~
}
```

</details>

<br>

---

<br>

<details>
<summary>✅ - Toggle examples of <strong>correct</strong> code for this rule</summary>

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Page({
  outputs: ['play', popstate, `online`, 'obsolete: obsol', 'store: storage'],
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component()
class Test {
  change = new EventEmitter();
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive()
class Test {
  @Output() buttonChange = new EventEmitter<'change'>();
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component({
  outputs,
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  outputs: [...test],
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component({
  outputs: func(),
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  outputs: [func(), 'a'],
})
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component({})
class Test {
  @Output() get getter() {}
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
const change = 'change';
@Component()
class Test {
  @Output(change) touchMove: EventEmitter<{ action: 'click' | 'close' }> = new EventEmitter<{ action: 'click' | 'close' }>();
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
const blur = 'blur';
const click = 'click';
@Directive()
class Test {
  @Output(blur) [click]: EventEmitter<Blur>;
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component({
  selector: 'foo[bar]'
})
class Test {
  @Output() bar: string;
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component({
  selector: '[foo], test',
})
class Test {
  @Output('foo') label: string;
}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/no-output-rename": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  selector: 'foo'
})
class Test {
  @Output('fooMyColor') myColor: string;
}
```

</details>

<br>