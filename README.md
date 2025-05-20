<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

   <h1>DeepfindCryoET -Protein-Complex-Annotation-Classification
</h1>

  <h2>Purpose</h2>
    <p>
        This code processes electron tomography (ET) data to identify and segment particles within 3D tomograms.
        The tool integrates <strong>Copick</strong> for particle detection and uses various algorithms for particle segmentation.
        It is designed for analyzing macromolecules, viruses, and other biological particles in electron microscopy datasets.
    </p>

  <h2>Key Features</h2>
    <ul>
        <li><strong>Tomogram Segmentation</strong>: Segments and identifies particles in 3D tomograms.</li>
        <li><strong>Particle Detection</strong>: Detects particles such as proteins, viruses, and other macromolecules.</li>
        <li><strong>Integration with Copick</strong>: Leverages <strong>Copick</strong> for identifying and processing particles based on their size and location.</li>
    </ul>

   <h2>Models and Techniques Used</h2>
    <h3>1. Copick</h3>
    <p>
        <strong>Copick Models</strong>: Used for identifying and processing pickable objects (particles) within the tomogram.
        It identifies particles based on their <strong>radius</strong> and location.
    </p>

   <h3>2. Denoising Algorithms</h3>
    <p>
        Applied to improve the quality of tomograms by removing noise, which helps in more accurate particle detection and segmentation.
    </p>

   <h3>3. Segmentation Models</h3>
    <p>
        <strong>Voxel-Based Segmentation</strong>: Uses voxel-based analysis to accurately segment particles by their size and spatial properties.
    </p>

   <h3>4. Machine Learning (Optional)</h3>
    <p>
        While the core process focuses on segmentation, <strong>ML models</strong> (such as <strong>scikit-learn</strong>) can be used for evaluating or classifying segmented data, though this is not the primary focus of the current code.
    </p>

  <h2>Output</h2>
    <p>Accuracy: 0.71 where as benchmark is 0.78    
<p>The output includes:</p>
    <ul>
        <li><strong>Particle Identification</strong>: A list of segmented particles with their names and radii.</li>
        <li><strong>Segmentation Data</strong>: Structured files that contain the particle data, ready for further analysis.</li>
        <li><strong>Visualization</strong>: Use of <strong>matplotlib</strong> for visualizing the segmentation results for inspection.</li>
    </ul>

   <p>Example output:</p>
    <pre>
        [('apo-ferritin', None, None, 6.0),
         ('beta-amylase', None, None, 6.5),
         ('beta-galactosidase', None, None, 9.0),
         ('ribosome', None, None, 15.0),
         ('thyroglobulin', None, None, 13.0),
         ('virus-like-particle', None, None, 13.5)]
    </pre>

   <h2>Input Parameters</h2>
    <ul>
        <li><strong>Voxel Size</strong>: Defines the size of each voxel in the tomogram data for accurate particle size estimation.</li>
        <li><strong>Tomogram Algorithm</strong>: Specifies the algorithm used to process and denoise the tomogram (e.g., 'denoised').</li>
        <li><strong>Output Settings</strong>: Configurable options for naming and identifying output files (e.g., output name, user ID, and session ID).</li>
    </ul>

  <h2>Installation</h2>
    <p>To set up the environment and install the necessary dependencies, run:</p>
    <pre>
        pip install deepfindET copick-utils matplotlib scikit-learn
    </pre>

</body>
</html>
