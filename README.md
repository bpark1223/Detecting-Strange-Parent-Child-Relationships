</h> Detecting Strange Parent-Child Relationships </h>
<h2>Description</h2>
In standard Windows environments, certain processes never call or spawn others. For example, it is unlikely to see "calc.exe" spawning "cmd.exe" in a normal Windows environment. Understanding these relationships can help to detect anomalies, which I will do in this exercise.
<h2>Utilities Used</h2>
</p>- Process Hacker</p>
</p>- Event Tracing for Windows</p>
<h2>Step-by-Step Walkthrough</h2>
</p> We can use Process Hacker to explore parent-child relationships within Windows. Sorting the processes by dropdowns in the Processes view reveals a hierarchical representation of the relationships.</p>
<img width="1438" alt="Screenshot 2024-07-03 at 4 46 13 PM" src="https://github.com/bpark1223/Detecting-Strange-Parent-Child-Relationships/assets/77799235/f775a9c4-0591-4b7c-832d-cf47bc87f492">
</p> Analyzing these relationships enables us to identify deviations from normal patterns. For example, if we observe the "spoolsv.exe" process creating "whoami.exe" instead of its expected behavior of creating a "conhost", it raises suspicion.
</p> 
