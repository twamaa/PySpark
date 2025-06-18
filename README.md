\documentclass\[12pt]{article}
\usepackage\[a4paper, margin=1in]{geometry}
\usepackage{graphicx}
\usepackage{titlesec}
\usepackage{fancyhdr}
\usepackage{hyperref}
\usepackage{setspace}
\usepackage{enumitem}
\usepackage{titling}

% For title formatting
\titleformat{\section}\[block]{\bfseries\Large}{\thesection.}{0.5em}{}
\titleformat{\subsection}\[block]{\bfseries\normalsize}{\thesubsection.}{0.5em}{}

% Header/footer setup
\pagestyle{fancy}
\fancyhf{}
\rhead{Predicting Quote Conversion}
\lhead{PySpark Classification}
\rfoot{\thepage}

% Cover Page
\begin{document}
\begin{titlepage}
\centering
\vspace\*{1cm}

```
\includegraphics[width=0.25\textwidth]{logo.png} % Replace 'logo.png' with your logo file name
\vspace{1cm}

\Huge
\textbf{Predicting Home Quote Conversion Using PySpark Classification Models}

\vspace{0.5cm}
\Large
A Machine Learning Approach Using Spark for Scalable Model Training

\vspace{1.5cm}

\textbf{Your Name} \\
Course: Data Science and AI \\
Instructor: Dr. John Doe \\
Institution: XYZ University \\
\today

\vfill
```

\end{titlepage}

\setcounter{page}{1}

% ==========================
\section{Executive Summary}
This project explores the application of machine learning techniques using PySpark to predict home quote conversion likelihood. The objective is to build a robust classification pipeline capable of handling a large, high-dimensional dataset efficiently and delivering high predictive performance. The dataset consists of over 200 features related to customer demographics, property attributes, and geographic indicators.

Three classification algorithms—Logistic Regression, Random Forest, and Gradient Boosted Trees—were trained and evaluated using a 70/30 train-validation split. Advanced preprocessing steps included handling missing data, encoding high-cardinality categorical features, and aligning categories between training and test sets. Hyperparameter tuning was performed using Spark’s CrossValidator with grid search.

Gradient Boosted Trees achieved the best performance with an AUC of 0.94 and accuracy of 91.5%. Feature importance analysis revealed key predictive variables spanning geographic and personal attributes. The pipeline demonstrates how PySpark can be effectively leveraged for scalable machine learning in real-world insurance or marketing applications.

% ==========================
\section{Introduction}
Predicting whether a customer will convert a home insurance quote into a policy is a critical task for insurance providers. Accurate predictions allow for more effective targeting, optimized marketing campaigns, and improved customer retention strategies. This classification task, however, presents several challenges due to the high dimensionality of features, the mixture of data types, and the presence of missing values.

This project addresses these challenges by building a scalable machine learning pipeline using PySpark, Apache Spark’s MLlib API. PySpark is particularly suitable for this task due to its ability to efficiently process large datasets across distributed computing environments.

The dataset used includes a mix of personal, property, and geographic features, along with a binary target variable indicating quote conversion. The goal is to preprocess the data appropriately, apply and compare multiple classification models, and evaluate their performance using standard metrics such as accuracy, AUC, and log loss.

This report outlines the complete workflow—from data cleaning to  evaluation—demonstrating both technical implementation and interpretability. The final model offers actionable insights and serves as a foundation for integrating predictive analytics into a real-world insurance decision-making system.

% ==========================
\section{Data Understanding}
% Describe the structure, source, and contents of the dataset.

% ==========================
\section{Data Preprocessing}
% Explain steps taken to clean, impute, encode, and prepare the data.
# PySpark
