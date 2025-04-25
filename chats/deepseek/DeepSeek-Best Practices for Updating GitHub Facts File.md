### User

i created a repo on github for add facts, details below

i added a file "facts.md" in master branch but i need to updating regularly. so let me know, what should i follow for best practice to change in master or create other branch if yes for other branch so, give me some real names to create branches to  update my facts file

---

### DeepSeek AI

<p class="ds-markdown-paragraph">It's great that you're thinking about best practices for maintaining your `facts.md` file! Since you'll be updating it regularly, here's what I recommend:</p><h3>Best Practice Approach:</h3><ol start="1"><li><p class="ds-markdown-paragraph"><strong>Avoid direct commits to `master`/`main` branch</strong> - This keeps your production content stable.</p></li><li><p class="ds-markdown-paragraph"><strong>Use feature branches</strong> - Create short-lived branches for each update, then merge via Pull Requests (PRs).</p></li></ol><h3>Suggested Branch Naming Strategy:</h3><p class="ds-markdown-paragraph">For a facts repository, you could use:</p>

<h4>Option 1: By Update Type</h4>

<pre>add-fact-&lt;topic&gt;
update-fact-&lt;ID&gt;
fix-fact-&lt;ID&gt;</pre>

<p class="ds-markdown-paragraph">Example:</p>

<pre>add-fact-space
update-fact-42
fix-fact-typo-17</pre>

<h4>Option 2: By Date</h4>

<pre>facts-update-YYYYMMDD</pre>

<p class="ds-markdown-paragraph">Example:</p>

<pre>facts-update-20231015</pre>

<h4>Option 3: By Category (if your facts are categorized)</h4>

<pre>facts/animals-add-lion
facts/science-update-quantum</pre></div><h3>Workflow Recommendation:</h3><ol start="1"><li><p class="ds-markdown-paragraph">Create a branch: `git checkout -b add-fact-space`</p></li><li><p class="ds-markdown-paragraph">Make your changes to `facts.md`</p></li><li><p class="ds-markdown-paragraph">Commit: `git commit -m "Add new fact about black holes"`</p></li><li><p class="ds-markdown-paragraph">Push: `git push origin add-fact-space`</p></li><li><p class="ds-markdown-paragraph">Create a Pull Request on GitHub</p></li><li><p class="ds-markdown-paragraph">Review your own changes (or have others review)</p></li><li><p class="ds-markdown-paragraph">Merge to master</p></li></ol><p class="ds-markdown-paragraph">This gives you:</p><ul><li><p class="ds-markdown-paragraph">A clean history</p></li><li><p class="ds-markdown-paragraph">Opportunity to review changes</p></li><li><p class="ds-markdown-paragraph">Easy revert if needed</p></li><li><p class="ds-markdown-paragraph">Better collaboration if others contribute later</p></li></ul><p class="ds-markdown-paragraph">For a solo project, this might seem like overkill, but it's good to build the habit, especially if the file grows large or gets more contributors later.</p>

---

### User

also give me some suggestion for commit message with following best practices

---

### DeepSeek AI

<p class="ds-markdown-paragraph">Great! Writing good commit messages is crucial for maintaining a clean, understandable project history. Here are some best practices and examples specifically tailored for your `facts.md` updates:</p><h3><strong>Commit Message Best Practices</strong> (Based on Conventional Commits &amp; Git Guidelines)</h3><ol start="1"><li><p class="ds-markdown-paragraph"><strong>Use the imperative mood</strong> ("Add fact" instead of "Added fact")</p></li><li><p class="ds-markdown-paragraph"><strong>Keep the subject line short</strong> (&lt;50 chars) and capitalize it</p></li><li><p class="ds-markdown-paragraph"><strong>Add a body (optional)</strong> if more explanation is needed (separated by a blank line)</p></li><li><p class="ds-markdown-paragraph"><strong>Use prefixes</strong> to indicate the type of change:</p><div class="markdown-table-wrapper"><table><thead><tr><th>Prefix</th><th>When to Use</th><th>Example</th></tr></thead><tbody><tr><td>`feat:`</td><td>New fact addition</td><td>`feat: Add quantum entanglement fact`</td></tr><tr><td>`fix:`</td><td>Correction to existing fact</td><td>`fix: Correct dinosaur extinction date`</td></tr><tr><td>`docs:`</td><td>Documentation updates (formatting, etc.)</td><td>`docs: Format facts in bullet points`</td></tr><tr><td>`chore:`</td><td>Maintenance (e.g., file reorganization)</td><td>`chore: Move animal facts to separate section`</td></tr></tbody></table></div></li></ol><hr><h3><strong>Good Examples for Your `facts.md` Updates:</strong></h3><h4><strong>1. Adding New Facts:</strong></h4><ul><li><p class="ds-markdown-paragraph">Short:</p>


<pre>feat: Add black hole information</pre></li><li><p class="ds-markdown-paragraph">With body:</p>

<pre>feat: Add Stephen Hawking's black hole theory

Explains Hawking radiation and its relation to 
entropy. Source: "A Brief History of Time" (1988).</pre>
</li>
</ul>
<h4><strong>2. Correcting Facts:</strong></h4><ul><li><p class="ds-markdown-paragraph">Short:</p>


<pre>fix: Correct human DNA percentage</pre></li><li><p class="ds-markdown-paragraph">With body:</p>

<pre>fix: Update human-chimp DNA similarity to 98.8%

Previous claim of 99% was outdated. Source: 
Nature Journal (2023).</pre></li></ul><h4><strong>3. Formatting/Organization:</strong></h4><ul><li><p class="ds-markdown-paragraph">Short:</p>


<pre>docs: Alphabetize animal facts section</pre></li><li><p class="ds-markdown-paragraph">With body:</p>

<pre>docs: Restructure facts into categories

- Added headers: # Animals, # Science, # History  
- Improved readability for contributors.</pre></li></ul><h4><strong>4. Typos/Misc:</strong></h4><ul><li><p class="ds-markdown-paragraph">Short:</p>

<pre>fix: Typo in 'accomodate' → 'accommodate'</pre>
</li></ul><hr><h3><strong>Pro Tip:</strong></h3><p class="ds-markdown-paragraph">Use `git commit -m "subject" -m "body"` for multi-line messages, or write them in a text editor (`git commit` without `-m`).</p><p class="ds-markdown-paragraph">Example terminal workflow:</p>

<pre><span class="token function">git</span> checkout <span class="token parameter variable">-b</span> add-fact-space
<span class="token comment"># Edit facts.md</span>
<span class="token function">git</span> <span class="token function">add</span> facts.md
<span class="token function">git</span> commit <span class="token parameter variable">-m</span> <span class="token string">"feat: Add zero-gravity effects on humans"</span> <span class="token parameter variable">-m</span> <span class="token string">"Covers muscle atrophy and fluid distribution. Source: NASA (2022)."</span>
<span class="token function">git</span> push origin add-fact-space</pre></div><p class="ds-markdown-paragraph">This makes your history readable and helps track changes if you ever need to revert or audit sources. Would you like me to tailor examples to specific types of facts you’re adding?</p>

