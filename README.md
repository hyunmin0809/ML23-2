<h1>Machine Learning 2023-2 - ML23-2</h1>

<h2>Features Extracted</h2>

<h3>data_pre_1.ipynb</h3>
<ul>
  <li>X1: Timestamp sequences representing the occurrence of network events.</li>
  <li>X2: Direction * packet size information extracted from the data.</li>
  <li>X3: Burst sequences calculated based on packet size changes.</li>
</ul>

<h3>Preprocessing Steps:</h3>
<ol>
  <li>Feature Extraction:
    <ul>
      <li>It iterates through the dataset and extracts relevant features X1, X2, and X3, along with corresponding labels y.</li>
    </ul>
  </li>
  <li>Feature Transformation:
    <ul>
      <li>It creates new features:
        <ul>
          <li><code>X1_1</code>: Calculates the average time interval between consecutive events in X1.</li>
          <li><code>X3_1</code>: Computes the average of the top 10 absolute values in the burst sequences in X3.</li>
        </ul>
      </li>
    </ul>
  </li>
</ol>
 
<br>
<h3>data_pre_2.ipynb</h3>
<ul>
  <li>X4: Cumulative packet sizes for each instance.</li>
  <li>X5: Number of incoming packets (Rank 1 categorical feature).</li>
  <li>X6: Number of outgoing packets as a fraction of the total number of packets (Rank 2 categorical feature).</li>
  <li>X7: Number of incoming packets as a fraction of the total number of packets (Rank 3 categorical feature).</li>
</ul>

<h3>Preprocessing Steps:</h3>
<ol>
  <li>Feature Extraction:
    <ul>
      <li>It iterates through the dataset and extracts X4, X5, X6, and X7 as categorical features, along with corresponding labels y.</li>
    </ul>
  </li>
  <li>Feature Transformation:
    <ul>
      <li>The script calculates cumulative packet sizes (X4) and the ratios of incoming and outgoing packets (X5, X6, X7).</li>
    </ul>
  </li>
</ol>

<br>
<h3>data_pre_3.ipynb</h3>
<ul>
  <li>X8: Standard deviation of the outgoing packet ordering list (Rank 4 categorical feature).</li>
  <li>X9: Number of outgoing packets (Rank 5 categorical feature).</li>
</ul>

<h3>Preprocessing Steps:</h3>
<ol>
  <li>Feature Extraction:
    <ul>
      <li>It iterates through the dataset and extracts X8 and X9 as additional categorical features, along with corresponding labels y.</li>
    </ul>
  </li>
</ol>
