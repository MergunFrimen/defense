Good afternoon. My name is Dominik Tichý and today I would like to present to you the results of my bachelor's thesis work. The topic of my thesis is "Modern visualization of partial atomic charges in Mol*".

Partial atomic charges are real numbers that are assigned to each atom within a molecule and together these charges describe the distribution of electron density among the atoms of a molecule. Partial atomic charges find many applications in the field of computational chemistry, for example, they are used in molecular docking or pharmacophore modeling.

It is important to note that partial atomic charges are only a theoretical concept and it is therefore impossible to measure them experimentally. It is however possible to calculate them using various calculation methods. Quantum mechanical methods produce the most accurate charges, however, they are extremely slow and computationally very expensive. On the other hand, empirical methods only approximate the charges and are therefore much faster than quantum mechanical methods.

Empirical methods are used in various tools, programs, and web applications for calculating partial atomic charges. Two examples of web applications are - Atomic Charge Calculator and Alpha Charges - both of which were developed at the Structural bioinformatics research group at the National Center for biomolecular research.

Both of these web applications use a visualizer called Litemol Viewer for visualizing the results of the calculations - namely for visualizing the structure which is colored by the partial atomic charges. The Litemol viewer is however no longer maintained and it was therefore necessary to replace it with it's modern replacement which is the Mol* viewer. However the Mol* viewer did not have support for visualizing partial atomic charges.

This brings us to the main goals of this thesis. Firstly, it was necessary to study the theory regarding partial atomic charges in order to get a better understanding of how they work. Secondly, it was necessary to extend the Mol* viewer with suppport for visualizing partial atomic charges. And lastly, the updated Mol* viewer needed to be integrated into the web applications.

Before we could implement the Mol* extension, it was necessary to come up with a way to store the structure and charge data in one file. We settled on using the mmCIF file format for this purpose. The mmCIF acronym stands for macromolecular crystalographic information file and it is the most widely used chemical file format in the field of computational chemistry. We extended the mmCIF format to include two new data fields for storing data about the partial atomic charges.

After that I created the extension for visualizing partial atomic charges and integrated it into the Mol* Viewer. If a user wants to use this extension to visualize partial atomic charges of a structure, they simply need to add the structure and charge data into one mmCIF file with the custom data fields, and then they just need to drag and drop this file into the Mol* Viewer which will automatically visualize the structure and color it by the partial atomic charges.

Here are some examples of the coloring by partial atomic charges for the same molecule which is visualized in 3 different 3D representations. Notice that the coloring uses two different color gradients. For negative charges the visualization uses a red-to-white color gradient and for positive charges it uses a white-to-blue color gradient.

After implementing the Mol* extension it was necessary to integrate it into the Atomic Charge Calculator and Alpha Charges web applications. The integration with Atomic Charge Calculator was straightforward and only required to simply swap out the Litemol Viewer for the updated Mol* Viewer and reconnect the UI controls to controls of the Mol* Viewer.

Additionally, the web application received a new feature which allows the user to calculate charges for multiple empirical methods on a single calculation request. Previously the user had to make multiple calculation requests to achieve the same results. This feature also allows the user to switch between the different calculated charges using the highlighted UI controls

Since both web applications share the same architecture, the integration of the Mol* Viewer into AlphaCharges was pretty much the same. The AlphaCharges application also received a new feature which is a new page to which the user is redirected whenever some atoms are detected to be problematic. On this page the user is presented with an error message that lists the problematic atoms together with a pop up text message which describes in more detail the specific problem. Additionally, the user can click on the name of an atom in the error message, which will then trigger the Mol* Viewer to zoom in on the atom as can be seen in this example.

Finally, the work done on the AlphaCharges web application directly contributed to a research paper which was published in the Nucleic Acids Research journal which is a biomolecular journal with a impact factor of over 19.

To summarize my work, I have created the Mol* extension for visualizing partial atomic charges, I have integrated the updated Mol* viewer into the Atomic Charge Calculator and AlphaCharges web applications, I have additionally extended the capabilities of both web applications, and lastly I have directly contributed with this work to a scientific research paper.

Thank you for your attention.