<body>
    <h1>Aircrack-ng Lab Walkthrough</h1>
    <h2>Introduction</h2>
    <p>This guide will walk you through the TryHackMe Aircrack-ng lab, teaching you how to crack a WPA/WPA2 pre-shared key (PSK) using Aircrack-ng. Ensure you have access to TryHackMe and the necessary tools installed.</p>
    - <b><a href="https://tryhackme.com/r/room/wifihacking101">TryHackMe Aircrack-ng Lab</a></b>
    <h2>Prerequisites</h2>
    <ul>
        <li><strong>TryHackMe Account:</strong> Ensure you have an account on TryHackMe.</li>
        <li><strong>Aircrack-ng:</strong> Install Aircrack-ng for cracking WPA/WPA2 PSKs.</li>
        <li><strong>Wordlist:</strong> Download a wordlist like <code>rockyou.txt</code> to use for the brute-force attack.</li>
    </ul>
    <h2>Steps</h2>
    <ol>
        <li><strong>Download Task Files</strong>
            <p>Navigate to the TryHackMe Aircrack-ng lab and download the provided task files. You should get a compressed file (e.g., <code>files.tar.gz</code>).</p>
        </li>
        <li><strong>Extract the PCAP File</strong>
            <p>Unzip the downloaded tar.gz file using the following command (replace <code>&lt;fileName&gt;</code> with the actual file name):</p>
            <pre><code>tar -xvzf &lt;fileName.tar.gz&gt;</code></pre>
            <img width="1171" alt="Screenshot 2024-05-21 at 5 49 35 PM" src="https://github.com/Fabiany-cs/Aircrack-ng-Suite/assets/107880960/96dfe316-dc89-4c9a-a178-e468052a44e5">
        </li>
        <li><strong>Identify the Extracted Files</strong>
            <p>After unzipping, you should see a <code>.cap</code> file which is a packet capture file containing the handshake data needed for cracking the PSK.</p>
        </li>
        <li><strong>Crack the PSK Using Aircrack-ng</strong>
            <p>Use Aircrack-ng to crack the PSK by providing the <code>.cap</code> file and the wordlist (e.g., <code>rockyou.txt</code>):</p>
            <pre><code>aircrack-ng &lt;fileName.cap&gt; -w /path/to/rockyou.txt</code></pre>
            <img width="1171" alt="Screenshot 2024-05-21 at 5 51 54 PM" src="https://github.com/Fabiany-cs/Aircrack-ng-Suite/assets/107880960/44639e9d-dc91-44dc-9a01-2fba754a868e">
            <p>Breakdown of the command:</p>
            <ul>
                <li><code>&lt;fileName.cap&gt;</code>: the packet capture file.</li>
                <li><code>-w /path/to/rockyou.txt</code>: specifies the path to the wordlist file.</li>
            </ul>
            <img width="1171" alt="Screenshot 2024-05-21 at 5 52 52 PM" src="https://github.com/Fabiany-cs/Aircrack-ng-Suite/assets/107880960/20135ce9-f556-4b7e-8b3a-f3741d8142d4">
        </li>
        <li><strong>Clean Up</strong>
            <p>After successfully cracking the PSK, clean up any downloaded or extracted files if necessary to keep your workspace organized:</p>
            <pre><code>rm &lt;fileName.tar.gz&gt;
rm &lt;fileName.cap&gt;</code></pre>
            <img width="1171" alt="Screenshot 2024-05-21 at 5 53 20 PM" src="https://github.com/Fabiany-cs/Aircrack-ng-Suite/assets/107880960/a82300d6-ba13-475c-a7b2-8bdca47fb8b7">
        </li>
    </ol>
    <h2>Conclusion</h2>
    <p>By following these steps, you can successfully use Aircrack-ng to crack a WPA/WPA2 PSK in the TryHackMe Aircrack-ng lab. Make sure to replace placeholder values with actual data from your lab environment.</p>
</body>
</html>
