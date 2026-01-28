<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hertz Lab - University of Michigan College of Pharmacy</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background-color: #00274c;
            color: white;
            padding: 20px 0;
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header-content h1 {
            font-size: 2em;
            margin-bottom: 5px;
        }

        .header-content p {
            font-size: 1.1em;
            color: #ffcb05;
        }

        /* Navigation */
        nav {
            background-color: #ffcb05;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        nav li {
            margin: 0 20px;
        }

        nav a {
            text-decoration: none;
            color: #00274c;
            font-weight: 600;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #666;
        }

        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        section {
            margin-bottom: 50px;
        }

        h2 {
            color: #00274c;
            font-size: 2em;
            margin-bottom: 20px;
            border-bottom: 3px solid #ffcb05;
            padding-bottom: 10px;
        }

        h3 {
            color: #00274c;
            font-size: 1.5em;
            margin-top: 25px;
            margin-bottom: 15px;
        }

        p {
            margin-bottom: 15px;
        }

        /* Links */
        a {
            color: #00274c;
            text-decoration: underline;
        }

        a:hover {
            color: #ffcb05;
        }

        /* Highlight Box */
        .highlight-box {
            background-color: #e8f4f8;
            border-left: 4px solid #00274c;
            padding: 20px;
            margin-top: 20px;
            border-radius: 5px;
        }

        .highlight-box p {
            margin-bottom: 0;
            font-weight: 600;
            color: #00274c;
        }

        /* Research Areas */
        .research-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 25px;
        }

        .research-card {
            background-color: #f5f5f5;
            padding: 30px;
            border-radius: 8px;
            border-left: 4px solid #00274c;
        }

        .research-card h3 {
            margin-top: 0;
            margin-bottom: 15px;
            color: #00274c;
        }

        .research-card p {
            margin-bottom: 10px;
        }

        .grant-info {
            background-color: #fff;
            padding: 15px;
            margin-top: 15px;
            border-radius: 5px;
            border-left: 3px solid #ffcb05;
        }

        .grant-info strong {
            color: #00274c;
        }

        .grant-info p {
            margin-bottom: 0;
        }

        .grant-info a {
            font-weight: 600;
        }

        /* Team Section */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 25px;
        }

        .team-member {
            text-align: center;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
        }

        .team-member.pi {
            background-color: #e8f4f8;
            border: 2px solid #00274c;
        }

        .team-member h4 {
            color: #00274c;
            margin: 0 0 15px 0;
            font-size: 1.2em;
        }

        .team-member .member-name {
            color: #00274c;
            margin: 5px 0;
            font-size: 1em;
        }

        .team-member .member-name a {
            text-decoration: none;
            color: #00274c;
            font-weight: normal;
        }

        .team-member .member-name a:hover {
            color: #ffcb05;
            text-decoration: underline;
        }

        .team-member p {
            color: #666;
            font-size: 0.95em;
            margin-bottom: 5px;
        }

        .team-member .title {
            font-weight: 600;
            color: #00274c;
        }

        /* Publications */
        .publication {
            background-color: #f9f9f9;
            padding: 20px;
            margin-bottom: 15px;
            border-radius: 5px;
            border-left: 4px solid #ffcb05;
        }

        .publication p {
            margin-bottom: 5px;
        }

        .publication-title {
            font-weight: 600;
            color: #00274c;
        }

        .publication-title a {
            color: #00274c;
            text-decoration: none;
        }

        .publication-title a:hover {
            color: #ffcb05;
            text-decoration: underline;
        }

        .publication-authors {
            color: #666;
            font-size: 0.95em;
        }

        .publication-journal {
            font-style: italic;
            color: #555;
        }

        .loading {
            text-align: center;
            padding: 20px;
            color: #666;
            font-style: italic;
        }

        .error {
            background-color: #ffe8e8;
            border-left: 4px solid #c00;
            padding: 15px;
            margin-top: 15px;
            border-radius: 5px;
            color: #c00;
        }

        /* News/Headlines List */
        .news-list {
            list-style-position: inside;
            margin-top: 20px;
        }

        .news-list li {
            margin-bottom: 12px;
            padding: 10px;
            background-color: #f9f9f9;
            border-radius: 5px;
            border-left: 3px solid #ffcb05;
        }

        .news-list li a {
            color: #00274c;
            text-decoration: none;
            font-weight: 500;
        }

        .news-list li a:hover {
            color: #ffcb05;
            text-decoration: underline;
        }

        /* Contact Section */
        .contact-info {
            background-color: #f5f5f5;
            padding: 30px;
            border-radius: 8px;
            margin-top: 25px;
        }

        .contact-info p {
            margin-bottom: 10px;
        }

        .contact-info strong {
            color: #00274c;
        }

        /* Footer */
        footer {
            background-color: #00274c;
            color: white;
            text-align: center;
            padding: 30px 20px;
            margin-top: 50px;
        }

        footer a {
            color: #ffcb05;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        /* Responsive */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }

            nav li {
                margin: 10px 0;
            }

            .header-content h1 {
                font-size: 1.5em;
            }

            .research-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <h1>Hertz Lab</h1>
            <p>University of Michigan College of Pharmacy</p>
        </div>
    </header>

    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#research">Research</a></li>
            <li><a href="#team">Team</a></li>
            <li><a href="#publications">Publications</a></li>
            <li><a href="#news">News</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <div class="container">
                <section id="about">
            <h2>About the Lab</h2>
            <p>The objective of the Hertz lab is to develop personalized cancer treatment approaches and translate them into clinical practice to optimize therapeutic outcomes in patients with cancer. Our research spans the translational spectrum from discovery through implementation. We identify clinical, kinetic, genetic, and physiologic predictors of cancer treatment efficacy and/or toxicity in retrospective analyses. These discoveries are integrated into novel tools that can be tested in prospective clinical trials to demonstrate that personalized cancer treatment enhances efficacy and/or prevents unnecessary toxicity.</p>
            
            <div style="text-align: center; margin: 30px 0;">
                <iframe width="560" height="315" src="https://www.youtube.com/embed/dRUBxrbLJKM?si=cOiWiOa5ZKXdqB9p" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen style="max-width: 100%; border-radius: 8px;"></iframe>
            </div>
            
            <div class="highlight-box">
                <p>My lab is accepting PhD students.</p>
            </div>
        </section>

        <section id="research">
            <h2>Research Focus</h2>
            
            <div class="research-grid">
                <div class="research-card">
                    <h3>DPYD Pharmacogenetics</h3>
                    <p>We investigate genetic variations in the DPYD gene that encodes the dihydropyrimidine dehydrogenase (DPD) enzyme to predict and prevent severe fluoropyrimidine toxicity in cancer patients, enabling safer and more personalized chemotherapy dosing strategies.</p>
                    
                    <div class="grant-info">
                        <p>Real-world analysis of clinical outcomes from DPYD-guided dosing (<a href="https://redcapproduction.umms.med.umich.edu/surveys/?s=CYX4873L7CR8LJM8" target="_blank">OPREC</a>)</p>
                    </div>
                    
                    <div class="grant-info">
                        <p><a href="https://test4dpd.org/" target="_blank">Advocacy</a> to increase clinical adoption of DPYD testing</p>
                    </div>
                </div>
                
                <div class="research-card">
                    <h3>Biomarkers of Chemotherapy-Induced Peripheral Neuropathy</h3>
                    <p>Our laboratory identifies predictive biomarkers for chemotherapy-induced peripheral neuropathy (CIPN) to help oncologists personalize treatment and minimize this debilitating toxicity that affects quality of life in cancer survivors.</p>
                    
                    <div class="grant-info">
                        <p><strong><a href="https://reporter.nih.gov/search/8Q96wlzo1kKXeKN_6xe9EQ/project-details/10757440" target="_blank">NCI R37 Grant</a>:</strong> Discovery and validation of predictive biomarkers of CIPN using the <a href="https://clinicaltrials.gov/study/NCT03939481" target="_blank">SWOG S1714</a> cohort.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="team">
            <h2>Our Team</h2>
            
            <div class="team-grid">
                <div class="team-member pi">
                    <h4>Principal Investigator</h4>
                    <p class="title"><a href="https://pharmacy.umich.edu/people/hertz-daniel/" target="_blank">Daniel L. Hertz, PharmD, PhD</a></p>
                    <p>Associate Professor of Clinical Pharmacy</p>
                </div>
                
                <div class="team-member">
                    <h4>PhD Students</h4>
                    <p class="member-name"><a href="https://pharmacy.umich.edu/people/kanji-comfort/" target="_blank">Comfort Kanji</a></p>
                    <p class="member-name"><a href="https://pharmacy.umich.edu/people/liu-yaping/" target="_blank">Yaping Liu</a></p>
                    <p class="member-name"><a href="https://pharmacy.umich.edu/people/nguyen-hoang-nam/" target="_blank">Nam Nguyen-Hoang</a></p>
                    <p class="member-name"><a href="https://pharmacy.umich.edu/people/sun-yuchen/" target="_blank">Yuchen Sun</a></p>
                </div>
                
                <div class="team-member">
                    <h4>Postdoctoral Fellows</h4>
                    <p class="member-name"><a href="https://pharmacy.umich.edu/people/granados-ii-javier/" target="_blank">Javier Granados II, PharmD</a></p>
                    <p class="member-name"><a href="https://pharmacy.umich.edu/people/slimano-florian/" target="_blank">Florian Slimano, PharmD</a></p>
                </div>
            </div>
        </section>

        <section id="publications">
            <h2>Recent Publications</h2>
            <div id="publications-container">
                <p class="loading">Loading publications from PubMed...</p>
            </div>
            <p style="margin-top: 20px;"><em>For a complete list of publications, visit <a href="https://pubmed.ncbi.nlm.nih.gov/?term=Hertz+DL%5BAuthor%5D&sort=date" target="_blank">PubMed</a>.</em></p>
            
            <h3 style="margin-top: 40px;">Recent PhD Student Publications</h3>
            <div id="student-publications-container">
                <p class="loading">Loading PhD student publications from PubMed...</p>
            </div>
        </section>

        <section id="news">
            <h2>Hertz Lab in the Headlines</h2>
            <ol class="news-list">
                <li><a href="https://www.pharmacytimes.com/view/dpyd-testing-gains-ground-nccn-guideline-update-reflects-decades-of-work-toward-safer-chemotherapy" target="_blank">DPYD Testing Gains Ground: NCCN Guideline Update Reflects Decades of Work Toward Safer Chemotherapy</a></li>
                <li><a href="https://www.michiganmedicine.org/news-release/research-and-advocacy-pays-fda-action-will-save-lives" target="_blank">Research and Advocacy Pays: FDA Action Will Save Lives</a></li>
                <li><a href="https://kffhealthnews.org/news/article/chemotherapy-drug-f5u-capecitabine-toxicity-test-death-prevention/" target="_blank">Chemotherapy Drug 5-FU/Capecitabine Toxicity Test Death Prevention</a></li>
                <li><a href="https://www.oncologynewscentral.com/article/fda-updates-safety-label-for-fluorouracil-injection-products" target="_blank">FDA Updates Safety Label for Fluorouracil Injection Products</a></li>
                <li><a href="https://www.michiganmedicine.org/health-lab/monitoring-program-flags-cancer-patients-risk-highly-toxic-chemotherapy-side-effects" target="_blank">Monitoring Program Flags Cancer Patients at Risk for Highly Toxic Chemotherapy Side Effects</a></li>
                <li><a href="https://www.captodayonline.com/time-for-wider-pretreatment-dpyd-genotyping/" target="_blank">Time for Wider Pretreatment DPYD Genotyping</a></li>
                <li><a href="https://oncologycompass.com/blog/post/vitamin-d-supplementation-plays-a-role-in-the-reduction-of-chemotherapy-toxicity" target="_blank">Vitamin D Supplementation Plays a Role in the Reduction of Chemotherapy Toxicity</a></li>
                <li><a href="https://www.oncologynewscentral.com/article/can-vitamin-d-help-prevent-paclitaxel-induced-peripheral-neuropathy" target="_blank">Can Vitamin D Help Prevent Paclitaxel-Induced Peripheral Neuropathy?</a></li>
                <li><a href="https://www.cancernetwork.com/view/lack-of-vitamin-d-may-increase-chemo-induced-neuropathy-risk-in-breast-cancer" target="_blank">Lack of Vitamin D May Increase Chemo-Induced Neuropathy Risk in Breast Cancer</a></li>
            </ol>
        </section>

        <section id="contact">
            <h2>Contact</h2>
            
            <h3>Prospective Students</h3>
            <p>We welcome inquiries from motivated students interested in clinical-translational cancer research. Please review the <a href="https://pharmacy.umich.edu/pharmacy-programs/phd/clinical-pharmacy-translation-science/" target="_blank">UM CPTS PhD Program</a> or contact <a href="https://pharmacy.umich.edu/people/hertz-daniel/" target="_blank">Dr. Hertz</a> directly for other opportunities in our laboratory.</p>
        </section>
    </div>

    <footer>
        <p>&copy; 2026 Hertz Lab - University of Michigan College of Pharmacy</p>
        <p><a href="https://pharmacy.umich.edu/">College of Pharmacy</a> | <a href="https://umich.edu/">University of Michigan</a></p>
    </footer>

    <script>
        // Function to fetch publications from PubMed
        async function fetchPublications() {
            const container = document.getElementById('publications-container');
            
            try {
                const searchUrl = 'https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=Hertz+DL[Author]&retmax=5&sort=date&retmode=json';
                
                const searchResponse = await fetch(searchUrl);
                const searchData = await searchResponse.json();
                
                if (!searchData.esearchresult || !searchData.esearchresult.idlist || searchData.esearchresult.idlist.length === 0) {
                    container.innerHTML = '<p class="error">No publications found.</p>';
                    return;
                }
                
                const pubmedIds = searchData.esearchresult.idlist;
                const summaryUrl = `https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id=${pubmedIds.join(',')}&retmode=json`;
                
                const summaryResponse = await fetch(summaryUrl);
                const summaryData = await summaryResponse.json();
                
                let publicationsHTML = '';
                
                pubmedIds.forEach(id => {
                    const pub = summaryData.result[id];
                    if (pub) {
                        const title = pub.title || 'No title available';
                        const authors = pub.authors ? pub.authors.map(a => a.name).join(', ') : 'No authors available';
                        const journal = pub.fulljournalname || pub.source || 'Journal information not available';
                        const year = pub.pubdate ? pub.pubdate.split(' ')[0] : '';
                        const volume = pub.volume || '';
                        const issue = pub.issue || '';
                        const pages = pub.pages || '';
                        
                        let citation = journal;
                        if (year) citation += `, ${year}`;
                        if (volume) citation += `, ${volume}`;
                        if (issue) citation += `(${issue})`;
                        if (pages) citation += `, ${pages}`;
                        
                        publicationsHTML += `
                            <div class="publication">
                                <p class="publication-title">
                                    <a href="https://pubmed.ncbi.nlm.nih.gov/${id}/" target="_blank">${title}</a>
                                </p>
                                <p class="publication-authors">${authors}</p>
                                <p class="publication-journal">${citation}</p>
                            </div>
                        `;
                    }
                });
                
                container.innerHTML = publicationsHTML;
                
            } catch (error) {
                console.error('Error fetching publications:', error);
                container.innerHTML = '<p class="error">Error loading publications. Please try again later or visit <a href="https://pubmed.ncbi.nlm.nih.gov/?term=Hertz+DL%5BAuthor%5D&sort=date" target="_blank">PubMed directly</a>.</p>';
            }
        }

        // Function to fetch PhD student publications
        async function fetchStudentPublications() {
            const container = document.getElementById('student-publications-container');
            
            try {
                const searchQuery = '(Hertz+DL[Author])+AND+(Liu+Y[Author]+OR+Kanji+C[Author]+OR+Nguyen-Hoang+N[Author]+OR+Sun+Y[Author])';
                const searchUrl = `https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=${searchQuery}&retmax=5&sort=date&retmode=json`;
                
                const searchResponse = await fetch(searchUrl);
                const searchData = await searchResponse.json();
                
                if (!searchData.esearchresult || !searchData.esearchresult.idlist || searchData.esearchresult.idlist.length === 0) {
                    container.innerHTML = '<p style="text-align: center; color: #666; font-style: italic;">No collaborative publications found yet.</p>';
                    return;
                }
                
                const pubmedIds = searchData.esearchresult.idlist;
                const summaryUrl = `https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id=${pubmedIds.join(',')}&retmode=json`;
                
                const summaryResponse = await fetch(summaryUrl);
                const summaryData = await summaryResponse.json();
                
                let publicationsHTML = '';
                
                pubmedIds.forEach(id => {
                    const pub = summaryData.result[id];
                    if (pub) {
                        const title = pub.title || 'No title available';
                        const authors = pub.authors ? pub.authors.map(a => a.name).join(', ') : 'No authors available';
                        const journal = pub.fulljournalname || pub.source || 'Journal information not available';
                        const year = pub.pubdate ? pub.pubdate.split(' ')[0] : '';
                        const volume = pub.volume || '';
                        const issue = pub.issue || '';
                        const pages = pub.pages || '';
                        
                        let citation = journal;
                        if (year) citation += `, ${year}`;
                        if (volume) citation += `, ${volume}`;
                        if (issue) citation += `(${issue})`;
                        if (pages) citation += `, ${pages}`;
                        
                        publicationsHTML += `
                            <div class="publication">
                                <p class="publication-title">
                                    <a href="https://pubmed.ncbi.nlm.nih.gov/${id}/" target="_blank">${title}</a>
                                </p>
                                <p class="publication-authors">${authors}</p>
                                <p class="publication-journal">${citation}</p>
                            </div>
                        `;
                    }
                });
                
                container.innerHTML = publicationsHTML;
                
            } catch (error) {
                console.error('Error fetching student publications:', error);
                container.innerHTML = '<p class="error">Error loading student publications. Please try again later.</p>';
            }
        }
        
        document.addEventListener('DOMContentLoaded', function() {
            fetchPublications();
            fetchStudentPublications();
        });
    </script>
</body>
</html>
