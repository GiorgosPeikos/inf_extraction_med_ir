# Investigating the Impact of Query Representation on Medical Information Retrieval

This repository contains the experiments related to the paper entitled "Investigating the Impact of Query Representation on Medical Information Retrieval", published in 

# Contents

1. [Folder Structure] Contains the topics for the collections related to Clinical Trials and the extracted query reformulations.
2. [Code] Medical Entities - Information Extraction Approaches.
3. [Code] Information Extraction & Query formulation.
4. [Code] Information Retrieval on TREC Clinical, Clinical Collection, TREC CDS Collections. 
5. [Information] 


# 1. Folder Structure
<ul>
  <li>experiments
  <ul>
    <li>indices</li>
       <ul>
         <li>Add the indices of TREC2021 clinical (trec_clc folder), the clinical collection (clinical floder). For the latter, refer to the paper for download details.</li>
         <li>CDS collections are obtained by ir_datasets.</li>
         <li>[sub-folder] trec_clc</li>
         <li>[sub-folder] clinical</li>
       </ul>
      <li>medical_entity_extraction</li>
       <ul>
          <li>Contains the notebooks that extract the medical entities, using the various libraries.</li>
        </ul>
      <li>qrels</li>
       <ul>
          <li>Add the TREC 2021 clinical qrels. [refer to TREC 2021 Clinical trials task.]</li>
          <li>Add the qrels related to the other clinical collection [Refer to the paper for download details.].</li>
          <li>For the CDS collections qrels are obtained by ir_datasets.</li>
        </ul>
      <li>topics
        <ul>
          <li>trec_clc
            <ul>
              <li>topics2021.txt : Contains the TREC 2021 topics.</li>
              <li>extracted_med_entities
                <ul>
                  <li>Here the ''method.csv'' files with the extracted medical entities will be saved using code 2. The entities have already been extracted.</li>
                  <li>chem_med7.csv : Entities extracted using med7</li>
                  <li>dis_chem_bio_bert.csv: Entities extracted using bio bert.</li>
                  <li>dis_chem_scispacy.csv : Entities extracted using scispacy.</li>
                  <li>dis_chem_stanza.csv : Entities extracted using stanza.</li>
                </ul>
              </li>
              <li>reformulated_topics
                <ul>
                  <li>Here the experiment_name.csv files with the reformulated topics, will be saved using code 3.</li>
                  <li>Format: ['qid','query','experiment_name']</li>
                  <li>experiment_name = {Q10bert_All_not_negated_NERs_keep_Sentences,...,bert_problems_treat_test_not_negated_Neg_BERT}</li>
                </ul>
              </li>
            </ul>
          </li>
          <li>cds_clinical
            <ul>
              <li>topics-2014_2015-description.topics : Contains the topics associated with the TREC cds collection and the other clinical collection.</li>
              <li>extracted_med_entities
                <ul>
                  <li>Here the ''method.csv'' files with the extracted medical entities will be saved using code 2. The entities have already been extracted.</li>
                  <li>chem_med7.csv : Entities extracted using med7</li>
                  <li>dis_chem_bio_bert.csv: Entities extracted using bio bert.</li>
                  <li>dis_chem_scispacy.csv : Entities extracted using scispacy.</li>
                  <li>dis_chem_stanza.csv : Entities extracted using stanza.</li>
                </ul>
              </li>
              <li>reformulated_topics
                <ul>
                  <li>Here the experiment_name.csv files with the reformulated topics, will be saved using code 3.</li>
                  <li>Dataframe Format: ['qid','query','experiment_name']</li>
                  <li>experiment_name = {Q10bert_All_not_negated_NERs_keep_Sentences,...,bert_problems_treat_test_not_negated_Neg_BERT}</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </li>
    </ul>
  </li>
</ul>


# 2. Medical Entities - Information Extraction Approaches.
To extract medical entities, for each topic, run the 4 notebooks in the medical_entity_extraction folder. 
<ul>
  <li> BioBert_disease.ipynb </li>
  <li> medical_extraction_m7.ipynb </li>
  <li> medical_extraction_stanza.ipynb </li>
  <li> scispacy.ipynb </li>

</ul>

In general, the notebooks have the following inputs and output: 
<ul>
  <li> A selected collection, among the four employed in this work. </li>
  <li> It reads the original versions of the queries, i.e., topics2021.txt or topics-2014_2015-description.topics. </li>
  <li> It saves in extracted entities in the extracted_med_entities folder. </li>
</ul>
Detailed instructions regarding their implementation are provided in each notebook.


# 3. Information Extraction & Query formulation.
The following notebook implements the information extraction an query reformulation approaches introduced in the paper. In addition it allows for all possible combinations of methods to be applied. 

<ul>
  <li> 1. Query_Reformulation_Techniques.ipynb </li>
</ul>

In general, it has the following inputs and output: 
<ul>
  <li> A collection, among the four employed in this work. </li>
  <li> It reads the original versions of the queries, i.e., topics2021.txt or topics-2014_2015-description.topics. </li>
  <li> It save in reformulated_topics, the desired topic reformulations. </li>
</ul>
Detailed instructions regarding its implementation are provided in the notebook.

# 4. Information Retrieval on TREC Clinical, Clinical Collection, TREC CDS Collections. 
<ul>
  <li> 1. TREC2021_Experiments.ipynb </li>
  <li> 1. Clinical_Experiments.ipynb </li>
  <li> 1. Clinical_Decision_Support_Track_2014_2015.ipynb </li>
</ul>

In general, the codes have the following inputs and output: 
<ul>
  <li> A collection, among the four employed in this work. </li>
  <li> It reads the original versions of the queries, one or more selected query variation and the index. </li>
  <li> Information retrieval using PyTerrier. </li>
</ul>




