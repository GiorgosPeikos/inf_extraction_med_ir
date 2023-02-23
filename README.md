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
      <li>qrels</li>
      <li>topics
        <ul>
          <li>trec_clc
            <ul>
              <li>topics2021.txt : Contains the TREC 2021 topics.</li>
              <li>extracted_med_entities
                <ul>
                  <li>Here the method.csv files with the extracted medical entities will be saved using code B.</li>
                  <li>chem_med7.csv : Entities extracted using med7</li>
                  <li>dis_chem_bio_bert.csv: Entities extracted using bio bert.</li>
                  <li>dis_chem_scispacy.csv : Entities extracted using scispacy.</li>
                  <li>dis_chem_stanza.csv : Entities extracted using stanza.</li>
                </ul>
              </li>
              <li>reformulated_topics
                <ul>
                  <li>Here the experiment_name.csv files with the reformulated topics, will be saved using code C.</li>
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
                  <li>Here the method.csv files with the extracted medical entities will be saved using code B.</li>
                  <li>chem_med7.csv : Entities extracted using med7</li>
                  <li>dis_chem_bio_bert.csv: Entities extracted using bio bert.</li>
                  <li>dis_chem_scispacy.csv : Entities extracted using scispacy.</li>
                  <li>dis_chem_stanza.csv : Entities extracted using stanza.</li>
                </ul>
              </li>
              <li>reformulated_topics
                <ul>
                  <li>Here the experiment_name.csv files with the reformulated topics, will be saved using code C.</li>
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


# 3. Information Extraction & Query formulation.
The following notebook implements the information extraction an query reformulation approaches introduced in the paper. In addition it allows for all possible combinations of methods to be applied. 

<ul>
  <li> 1. Query_Reformulation_Techniques.ipynb <\li>
<\ul>

Detailed instructions regarding its implementation are provided in the notebook. In general, it has the following inputs and output: 
<ul>
  <li> A collection, among the four employed in this work. <\li>
  <li> It reads the original versions of the queries, i.e., topics2021.txt or topics-2014_2015-description.topics. <\li>
  <li> It save in reformulated_topics, the desired topic reformulations. <\li>
<\ul>


# 4. Information Retrieval on TREC Clinical, Clinical Collection, TREC CDS Collections. 






