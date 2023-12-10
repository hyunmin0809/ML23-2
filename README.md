# ML23-2
Machine Learning 2023-2


<h2>Features Extracted</h2>

<h3>data_pre_1.ipynb<h3>
<ul>
  <li><strong>X1:</strong> Timestamp sequences representing the occurrence of network events.</li>
  <li><strong>X2:</strong> Direction * packet size information extracted from the data.</li>
  <li><strong>X3:</strong> Burst sequences calculated based on packet size changes.</li>
</ul>

<h3>Preprocessing Steps:</h3>
<ol>
  <li><strong>Loading Data:</strong>
    <ul>
      <li>The script loads network data from a pickle file containing information about network packet sequences.</li>
    </ul>
  </li>
  <li><strong>Feature Extraction:</strong>
    <ul>
      <li>It iterates through the dataset and extracts relevant features X1, X2, and X3, along with corresponding labels y.</li>
    </ul>
  </li>
  <li><strong>Feature Transformation:</strong>
    <ul>
      <li>It creates new features:
        <ul>
          <li><code>X1_1</code>: Calculates the average time interval between consecutive events in X1.</li>
          <li><code>X3_1</code>: Computes the average of the top 10 absolute values in the burst sequences in X3.</li>
        </ul>
      </li>
    </ul>
  </li>
 

<h3>Note:</h3>
<ul>
  <li>This code serves as a preprocessing step for network data classification tasks.</li>
  <li>It assumes a specific format of input data and label assignment.</li>
</ul>
