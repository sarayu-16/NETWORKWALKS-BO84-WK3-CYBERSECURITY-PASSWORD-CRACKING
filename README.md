# NETWORKWALKS-BO84-WK3-CYBERSECURITY-PASSWORD-CRACKING
Password Cracking – Cybersecurity Lab (Week 3)
This repository documents two practical cybersecurity lab modules that demonstrate how password-protected PDF files can be audited in an authorized environment.

The project covers two approaches:
1. Project Module 1 – John the Ripper (JTR) and Johnny GUI
2. Project Module 2 – Networkwalks Hash Calculator and Password Cracker

Both exercises use a sample password-protected PDF (My Locked PDF1.pdf) and demonstrate the workflow of extracting a PDF password hash, testing it with a password-recovery tool, and verifying the recovered password by opening the PDF.
Important: Use these techniques only on files that you own or have explicit permission to test. Do not attempt to access another person's protected files or accounts.

Repository contents
password-cracking-lab/
├── README.md
├── Module-1-John-the-Ripper/
│   └── (Add your screenshots and lab notes here)
└── Module-2-Networkwalks-Tools/
    └── (Add your screenshots and lab notes here)

You can rename the folders to match the files you upload to GitHub. The two training PDFs can be added to the repository if you have permission to redistribute them. Avoid uploading the protected sample PDF, extracted hashes, or recovered passwords if they contain private information.

Module 1: Password Cracking with John the Ripper
Objective
Use John the Ripper and its graphical interface, Johnny, to audit the password strength of an authorized password-protected PDF.
Tools and resources
- John the Ripper – official website
- Johnny GUI – official project page
- Online PDF Hash Extractor referenced in the lab guide

Workflow
1. Download and install John the Ripper for your operating system.
2. Download and install Johnny GUI.
3. Open Johnny and go to Settings.
4. Browse to the John the Ripper executable (john.exe, located in the JTR run folder on Windows).
5. Obtain the PDF hash from the authorized sample PDF using a PDF hash-extraction utility.
6. Copy the complete hash. The lab guide notes that the hash should begin with $pdf$; remove any extra formatting characters if present.
7. Paste the hash into a text file and save it as hash1.txt.
8. In Johnny, choose Open password file and select hash1.txt.
9. Select Start new attack and allow the audit to run.
10. When a candidate password is recovered, use it to open the sample PDF and verify the result.

Expected learning outcome: Understand how John the Ripper processes password hashes and how a graphical interface can make a password-auditing workflow easier to operate.

Module 2: Password Cracking with Networkwalks Tools

Objective
Use Networkwalks' browser-based tools to extract a PDF hash and run a dictionary-based password audit without installing a desktop cracking application.
Tools and resources
- Networkwalks lab page
- Networkwalks Hash Calculator
- Networkwalks Password Cracker

Workflow
1. Download the authorized sample PDF from the lab page.
2. Open the Networkwalks Hash Calculator in a web browser.
3. Upload the protected PDF using the file option.
4. Copy the complete extracted PDF hash, including the $pdf$ prefix.
5. Open the Networkwalks Password Cracker.
6. Paste the hash into the PDF hash field.
7. Use the available built-in wordlist or upload an authorized wordlist, then start the cracking test.
8. Wait for the tool to finish. If a matching candidate is found, the result is displayed on the page.
9. Enter the recovered password into the sample PDF to verify that it opens.
Expected learning outcome: Understand the relationship between PDF hash extraction and dictionary-based password auditing, and observe a browser-based alternative to a locally installed tool.

Key concepts learned
- Password hashing: A password hash is a transformed representation used by a system to verify a password.
- Hash extraction: A compatible tool can extract the information needed by a password-auditing program from a protected PDF.
- Dictionary attack: A tool tests candidate passwords from a wordlist and checks whether a candidate matches the extracted hash.
- Password strength: Short, common, or predictable passwords are generally easier to guess than long, unique passwords.
- Encryption vs. hashing: Encryption is designed to be reversible with the appropriate key; cryptographic hashing is designed as a one-way transformation.

Comparison of the two modules
Feature	Module 1: JTR + Johnny	Module 2: Networkwalks Tools
Interface	Desktop application with GUI	Web browser
Hash extraction	External PDF hash-extraction utility, as described in the lab	Networkwalks Hash Calculator
Password audit	John the Ripper through Johnny	Networkwalks Password Cracker
Installation	JTR and Johnny must be installed	No local cracking-tool installation required
Attack approach	Configured through John/Johnny	Dictionary attack using the available or uploaded wordlist


Security recommendations
- Use long, unique passwords and avoid common words or predictable patterns.
- Do not reuse passwords across accounts or documents.
- Store passwords in a reputable password manager.
- Keep sensitive documents and extracted hashes private.
- Before uploading a document to an online hash-extraction service, review its privacy and data-retention terms. Prefer a trusted local tool for confidential files.
- Run password audits only with clear authorization.
Notes
- The training guides use the sample filename My Locked PDF1.pdf.
- The sample result shown in the Networkwalks guide is password1; this is an example from the training material, not a guarantee that another PDF will have the same password.
- Cracking time depends on the password, hash format, attack configuration, wordlist, and available computing resources.
- This README summarizes the two supplied Week 3 project-module guides. Add your own screenshots, observations, and results before presenting the repository as your completed practical work.
