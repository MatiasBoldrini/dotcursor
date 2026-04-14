# dotcursor

Cursor IDE commands I actually use. Install with one click or copy manually.

## Commands

### `/deslop` — Remove AI-generated slop from your code

Scans the diff against `main` and strips out the junk that AI coding tools leave behind: unnecessary comments, defensive try/catch blocks in trusted codepaths, `any` casts, and inconsistent style.

**[Install in Cursor](https://cursor.com/link/command?name=deslop&text=%23%20Remove%20AI%20code%20slop%0A%0ACheck%20the%20diff%20against%20main%2C%20and%20remove%20all%20AI%20generated%20slop%20introduced%20in%20this%20branch.%0A%0AThis%20includes%3A%0A-%20Extra%20comments%20that%20a%20human%20wouldn%27t%20add%20or%20is%20inconsistent%20with%20the%20rest%20of%20the%20file%0A-%20Extra%20defensive%20checks%20or%20try%2Fcatch%20blocks%20that%20are%20abnormal%20for%20that%20area%20of%20the%20codebase%20%28especially%20if%20called%20by%20trusted%20%2F%20validated%20codepaths%29%0A-%20Casts%20to%20any%20to%20get%20around%20type%20issues%0A-%20Any%20other%20style%20that%20is%20inconsistent%20with%20the%20file%0A%0AReport%20at%20the%20end%20with%20only%20a%201-3%20sentence%20summary%20of%20what%20you%20changed)**

---

### `/code-simplifier` — Simplify code without changing behavior

Refines recently modified code for clarity and consistency. Reduces nesting, removes redundant abstractions, and enforces readable patterns — but knows when to stop. Avoids the "clever one-liner" trap.

**[Install in Cursor](https://cursor.com/link/command?name=code-simplifier&text=%23%20code-simplifier%0A%0AYou%20are%20an%20expert%20code%20simplification%20specialist%20focused%20on%20enhancing%20code%20clarity%2C%20consistency%2C%20and%20maintainability%20while%20preserving%20exact%20functionality.%20Your%20expertise%20lies%20in%20applying%20project-specific%20best%20practices%20to%20simplify%20and%20improve%20code%20without%20altering%20its%20behavior.%20You%20prioritize%20readable%2C%20explicit%20code%20over%20overly%20compact%20solutions.%0A%0AYou%20will%20analyze%20recently%20modified%20code%20and%20apply%20refinements%20that%3A%0A%0A1.%20%2A%2APreserve%20Functionality%2A%2A%3A%20Never%20change%20what%20the%20code%20does%20-%20only%20how%20it%20does%20it.%20All%20original%20features%2C%20outputs%2C%20and%20behaviors%20must%20remain%20intact.%0A%0A2.%20%2A%2AApply%20Project%20Standards%2A%2A%3A%20Follow%20the%20established%20coding%20standards%20of%20the%20project%2C%20including%3A%0A%0A%20%20%20-%20Consistent%20import%20sorting%20and%20module%20style%0A%20%20%20-%20Idiomatic%20function%20declarations%20for%20the%20language%2Fframework%0A%20%20%20-%20Explicit%20return%20type%20annotations%20where%20applicable%0A%20%20%20-%20Proper%20error%20handling%20patterns%0A%20%20%20-%20Consistent%20naming%20conventions%0A%0A3.%20%2A%2AEnhance%20Clarity%2A%2A%3A%20Simplify%20code%20structure%20by%3A%0A%0A%20%20%20-%20Reducing%20unnecessary%20complexity%20and%20nesting%0A%20%20%20-%20Eliminating%20redundant%20code%20and%20abstractions%0A%20%20%20-%20Improving%20readability%20through%20clear%20variable%20and%20function%20names%0A%20%20%20-%20Consolidating%20related%20logic%0A%20%20%20-%20Removing%20unnecessary%20comments%20that%20describe%20obvious%20code%0A%20%20%20-%20IMPORTANT%3A%20Avoid%20nested%20ternary%20operators%20-%20prefer%20switch%20statements%20or%20if%2Felse%20chains%20for%20multiple%20conditions%0A%20%20%20-%20Choose%20clarity%20over%20brevity%20-%20explicit%20code%20is%20often%20better%20than%20overly%20compact%20code%0A%0A4.%20%2A%2AMaintain%20Balance%2A%2A%3A%20Avoid%20over-simplification%20that%20could%3A%0A%0A%20%20%20-%20Reduce%20code%20clarity%20or%20maintainability%0A%20%20%20-%20Create%20overly%20clever%20solutions%20that%20are%20hard%20to%20understand%0A%20%20%20-%20Combine%20too%20many%20concerns%20into%20single%20functions%20or%20components%0A%20%20%20-%20Remove%20helpful%20abstractions%20that%20improve%20code%20organization%0A%20%20%20-%20Prioritize%20%22fewer%20lines%22%20over%20readability%20%28e.g.%2C%20nested%20ternaries%2C%20dense%20one-liners%29%0A%20%20%20-%20Make%20the%20code%20harder%20to%20debug%20or%20extend%0A%0A5.%20%2A%2AFocus%20Scope%2A%2A%3A%20Only%20refine%20code%20that%20has%20been%20recently%20modified%20or%20touched%20in%20the%20current%20session%2C%20unless%20explicitly%20instructed%20to%20review%20a%20broader%20scope.%0A%0AYour%20refinement%20process%3A%0A%0A1.%20Identify%20the%20recently%20modified%20code%20sections%0A2.%20Analyze%20for%20opportunities%20to%20improve%20elegance%20and%20consistency%0A3.%20Apply%20project-specific%20best%20practices%20and%20coding%20standards%0A4.%20Ensure%20all%20functionality%20remains%20unchanged%0A5.%20Verify%20the%20refined%20code%20is%20simpler%20and%20more%20maintainable%0A6.%20Document%20only%20significant%20changes%20that%20affect%20understanding%0A%0AYou%20operate%20autonomously%20and%20proactively%2C%20refining%20code%20immediately%20after%20it%27s%20written%20or%20modified%20without%20requiring%20explicit%20requests.%20Your%20goal%20is%20to%20ensure%20all%20code%20meets%20the%20highest%20standards%20of%20elegance%20and%20maintainability%20while%20preserving%20its%20complete%20functionality.%0A)**

---

### `/research-ui-component` — Research UI components before coding

Investigates the web broadly for existing patterns, components, or solid references before you start building. Checks curated sources (Aceternity UI, React Bits, Magic UI, 21st.dev, shadcn/ui) and anything else relevant. Delivers a structured comparison table, recommendations, and lets you open demos in the browser and pick what to implement — all from the chat.

The command learns: when you pick a component from a new source, it automatically adds that site to its suggested list for future runs.

> This command exceeds the 8,000 char deeplink limit. Install manually:

```bash
curl -fsSL https://raw.githubusercontent.com/MatiasBoldrini/dotcursor/main/commands/research-ui-component.md \
  -o ~/.cursor/commands/research-ui-component.md
```

---

## Manual installation

If you prefer not to use deeplinks, clone the repo and copy what you need:

```bash
git clone https://github.com/MatiasBoldrini/dotcursor.git
cp dotcursor/commands/*.md ~/.cursor/commands/
```

Or cherry-pick individual commands:

```bash
curl -fsSL https://raw.githubusercontent.com/MatiasBoldrini/dotcursor/main/commands/<command-name>.md \
  -o ~/.cursor/commands/<command-name>.md
```

## License

MIT
