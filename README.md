<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Radiology Q&A | أسئلة وأجوبة في الأشعة</title>
    <!-- Tailwind CSS for styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts for better typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Apply Inter font to the body, which is good for English text */
        body {
            font-family: 'Inter', sans-serif;
        }
        /* Apply Cairo font for elements that will contain Arabic text */
        .font-cairo {
            font-family: 'Cairo', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-gray-900 text-gray-800 dark:text-gray-200">

    <!-- Main container for the content -->
    <div class="container mx-auto p-4 sm:p-6 lg:p-8">
        
        <!-- Header Section -->
        <header class="text-center mb-10">
            <h1 class="text-4xl lg:text-5xl font-bold text-gray-900 dark:text-white font-cairo" dir="rtl">أسئلة وأجوبة في الأشعة</h1>
            <p class="text-lg text-gray-600 dark:text-gray-400 mt-2 font-cairo" dir="rtl">مراجعة شاملة لمفاهيم الأشعة التشخيصية</p>
        </header>

        <!-- Grid container for the Q&A cards -->
        <main id="qa-container" class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-6">
            <!-- Question and answer cards will be dynamically injected here by the script -->
        </main>

    </div>

<script>
    // This script will parse the Q&A text and generate the HTML cards
    
    // The raw text containing all questions and answers
    const qaData = `
1. Definition of a neoplasm:
Abnormal tissue growth due to uncoordinated cellular proliferation.
2. Tumor classification (benign vs malignant) is based on:
Behavior.
3. Tumor with clear fat content on imaging:
Lipoma.
4. HCC contrast enhancement pattern:
Early arterial enhancement with portal washout.
5. Imaging modality contraindicated in cochlear implants:
MRI.
6. Bone change from benign tumor:
Scalloping (smooth erosion).
7. Feature suggesting malignant bone tumor:
"Onion peel" periosteal reaction.
8. Investigation of choice for RCC staging:
CT with IV contrast.
9. Most common age group for Wilms tumor:
Children.
10. Common presentation of bladder TCC:
Hematuria.
11. "Apple core" appearance on barium enema is seen in:
Colon cancer.
12. Diagnostic imaging finding in linitis plastica:
Diffuse gastric wall thickening.
13. Best diagnostic method for HCC:
Triphasic CT.
14. Mammographic finding suggestive of breast carcinoma:
Spiculated mass with microcalcifications.
15. Tumor with "shouldering sign" on barium swallow:
Esophageal carcinoma.
16. Primary role of ultrasound in Wilms tumor:
Distinguish solid from cystic masses.
17. Contraindication for IV contrast in CT:
Renal impairment.
18. Features differentiating benign from malignant tumors:
All of the above (slow growth, well-defined margins, displacement).
19. Codman’s triangle on X-ray is seen in:
Osteosarcoma.
20. Multicentric breast cancer involves:
Lesions in different quadrants
21. Which imaging modality is ideal for detecting dilated bile ducts in pancreatic carcinoma?
b) Ultrasound
22. The "shouldering sign" on barium swallow is seen in:
a) Esophageal carcinoma
23. Which tumor type is associated with submucosal spread causing "linitis plastica"?
b) Diffuse-type gastric adenocarcinoma
24. A painless abdominal mass in a child is most suggestive of:
b) Wilms tumor
25. Hypertension in a child with a renal mass is due to:
b) Excessive renin production
26. Which imaging feature distinguishes solid from cystic renal masses in Wilms tumor?
b) Ultrasound
27. Transitional cell carcinoma (TCC) of the bladder on CT may show:
a) Calcifications within the mass
28. The triad of hematuria, flank pain, and a palpable mass is classic for:
a) Renal cell carcinoma
29. Which imaging finding is diagnostic of liver metastases?
b) Hypodense or hyperdense focal lesions
30. The primary contraindication for MRI is:
c) Cardiac pacemaker
31. Which tumor shows "early arterial enhancement with portal washout" on triphasic CT?
b) Hepatocellular carcinoma (HCC)
32. A mammographic "spiculated mass with microcalcifications" suggests:
b) Breast carcinoma
33. The apple core appearance on barium enema is seen in:
c) Colon cancer
34. Which imaging feature is not associated with benign bone tumors?
c) Codman's triangle
35. The most common primary bladder tumor is:
c) Transitional cell carcinoma (TCC)
36. Which factor is critical when selecting ultrasound over MRI for imaging?
b) Cost
37. Aggressive periosteal reactions (e.g., "onion peel") are seen in:
b) Ewing's sarcoma
38. The main advantage of tumor characterization by imaging is:
a) Reducing biopsies
39. Which tumor is linked to intact cortex on X-ray (Figure 14)?
b) Aneurysmal bone cyst
40. In pancreatic carcinoma, triphasic CT is used to assess:
b) Relation to mesenteric vessels
41. Which tumor type arises from embryonic nephrogenic tissue?
b) Wilms tumor
42. The most common urinary system tumor is:
b) Bladder TCC
43. A fungating cauliflower-like mass in the esophagus is characteristic of:
b) Squamous cell carcinoma
44. Which imaging modality detects tumoral metabolites for characterization?
b) MRI spectroscopy
45. Which feature is not seen in malignant bone tumors?
c) Thin sclerotic rim
46. The initial imaging study for suspected Wilms tumor is:
b) Ultrasound
47. Which tumor type is hormone-producing?
b) Insulinoma
48. "Linitis plastica" refers to:
a) Gastric wall thickening and luminal narrowing
49. Which imaging finding indicates malignancy in breast lesions?
b) Grouped microcalcifications
50. The most common renal tumor in adults is:
c) Renal cell carcinoma
51. Which tumor is associated with fat content besides lipoma?
b) Renal angiomyolipoma
52. A heterogeneously enhancing left renal mass on CT is likely:
b) Renal cell carcinoma
53. The key purpose of chest X-ray in Wilms tumor is to detect:
c) Pulmonary metastases
54. Which tumor is not classified as epithelial in origin?
c) Lipoma
55. The hallmark of HCC on triphasic CT is:
c) Arterial phase enhancement with venous washout
56. Which factor is not considered when ordering imaging?
b) Tumor size
57. A circumferential mural thickening of the stomach on CT suggests:
b) Linitis plastica
58. Which imaging modality is best for detecting peritoneal spread in pancreatic cancer?
b) CT
59. The most common renal tumor in children is:
b) Wilms tumor
60. Which tumor type is not classified by histogenesis?
c) Benign
61. A scirrhous lesion in the esophagus appears as:
b) Annular stricture
62. Which tumor is not typically hypervascular?
c) Pancreatic carcinoma
63. The primary role of PET scan in HCC is to detect:
c) Distant metastases
64. Which tumor is linked to hydronephrosis due to ureteral obstruction?
a) Bladder TCC
65. A soft-tissue mass in the right upper lung lobe on CT suggests:
a) Bronchogenic carcinoma
66. Which feature is not seen in benign tumors?
c) Bone destruction
67. Which imaging finding supports multicentric breast cancer?
a) Lesions in multiple quadrants
68. A heterogeneous pancreatic head mass on CT is indicative of:
c) Pancreatic carcinoma
69. The first-line imaging for suspected bladder TCC is:
b) CT urography
70. Which tumor is not associated with calcifications?
d) Lipoma
71. The main limitation of ultrasound in pancreatic imaging is:
a) Overlying bowel gas
72. Which tumor type is classified as mesenchymal?
b) Lipoma
73. A focal hepatic lesion with fat density on CT is likely:
c) Angiomyolipoma
74. Which tumor marker is not linked to imaging follow-up?
d) Hemoglobin
75. The key feature of malignant ulcer in the stomach is:
b) Raised, everted edges
76. Which imaging modality is best for assessing renal vein invasion?
b) CT with contrast
77. The most common cause of "apple core" colon lesion is:
b) Adenocarcinoma
78. Which tumor is not typically cystic?
d) Lipoma
79. The primary use of bone scan in renal cell carcinoma is to detect:
c) Bone metastases
80. Which tumor is associated with paraneoplastic syndromes?
a) Renal cell carcinoma
81. Which imaging modality is contraindicated in the first trimester of pregnancy?
c) CT
82. The main advantage of MRI over CT in liver imaging is:
a) Better soft-tissue contrast
83. A hypodense liver lesion on CT may represent:
b) Metastasis
84. Which tumor is hormonally inactive?
c) Lipoma
85. The primary imaging finding in osteosarcoma is:
b) Codman's triangle
86. Which tumor is not associated with hemorrhage on imaging?
c) Fibroadenoma
87. The most specific sign of cavernous hemangioma on MRI is:
a) Peripheral nodular enhancement
88. Which tumor is not classified by gross appearance?
d) Pleomorphic
89. The gold standard for breast cancer diagnosis is:
b) Biopsy
90. Which imaging finding is not seen in HCC?
d) Fat density
91. A heterogeneous renal mass with necrosis is typical of:
c) Renal cell carcinoma
92. Which feature is not used to classify neoplasms?
b) Patient age
93. The primary imaging modality for detecting bone metastases is:
c) Bone scan
94. Which tumor is least likely to metastasize to bone?
d) Lipoma
95. The most common site for esophageal carcinoma is:
c) Lower third
    `;

    // Get the container element where the cards will be placed
    const container = document.getElementById('qa-container');
    
    // Split the data into individual Q&A pairs.
    // The regex splits by a newline that is followed by a number and a dot, ensuring each question starts a new block.
    const pairs = qaData.trim().split(/\n(?=\d+\.)/);

    // Loop through each pair to create and append a card
    pairs.forEach(pair => {
        const lines = pair.trim().split('\n');
        // Ensure the pair has at least a question and one answer line
        if (lines.length >= 2) {
            const question = lines[0].trim();
            // The answer is all the remaining lines, joined back together. 
            // This handles answers that might have multiple lines, although in this case they don't.
            const answer = lines.slice(1).join('\n').trim();

            // Create the main card container
            const card = document.createElement('div');
            card.className = "p-6 bg-white dark:bg-gray-800 rounded-2xl shadow-md transition-all duration-300 hover:shadow-xl hover:-translate-y-1";

            // Create the element for the question text
            const questionEl = document.createElement('p');
            questionEl.className = "text-md font-semibold text-gray-800 dark:text-white mb-4";
            questionEl.textContent = question;

            // Create a paragraph for the answer
            const answerEl = document.createElement('p');
            answerEl.className = "text-gray-700 dark:text-gray-300";
            
            // Create a span for the answer text to apply the highlight
            const spanEl = document.createElement('span');
            spanEl.className = "bg-yellow-300 dark:bg-yellow-400 px-3 py-1.5 rounded-lg text-gray-900 font-medium";
            spanEl.textContent = answer;

            // Assemble the card
            answerEl.appendChild(spanEl);
            card.appendChild(questionEl);
            card.appendChild(answerEl);
            
            // Add the completed card to the main grid
            container.appendChild(card);
        }
    });
</script>

</body>
</html>

