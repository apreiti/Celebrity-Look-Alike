# Celebrity-Look-Alike

The idea behind this project is to create a model that finds which celebrity you are the doppelg¨anger of,
based on your unique facial features.

We assumed that facial features alone might not be sufficient for accurate matching. Therefore, we explored additional traits, such as hair color, cheekbone position and gender, to
enhance the model’s precision. Leveraging the CelebA dataset on Kaggle, which provides a rich collection of celebrity images annotated with various facial attributes, we aimed to
create a higher understanding of each person’s appearance.

Our project unfolds in two fundamental steps. Firstly, we gathered comparison images byscraping thumbnail images from Wikipedia celebrity pages. Then, we used the face recognition
library to effortlessly obtain facial bounding boxes, setting the groundwork for a reliable baseline that would later be enriched. The baseline consisted in computing the similarity of the
bounding boxes of the input faces with respect to the dataset ones, without using any featuremodel to enhance the performance.

In the next phase, we trained three distinct deep learning models to address the nuances of specific facial traits.

• For hair color classification, a customized CNN was built.
• To tackle gender detection, we used InceptionV3 net fine-tuned for our specific use case.
• Lastly, we created a model to detect high cheekbones using the MobileNetV2 model.

These deep learning models, trained on a subset of CelebA, were integrated into ourpipeline. The resulting ensemble, comprising the baseline and refined models, presented a
solution for celebrity look alike problem.
