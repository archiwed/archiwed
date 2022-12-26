## Olá, eu sou André

```python

#!/usr/bin/env python
import profile
import description

AUTHOR = config['andrxduarte']['author']
AUTHOR_EMAIL = config['andrxduarte']['email']

with open('README.md') as text:
    LONG_DESCRIPTION = text.read()

REQUIREMENTS = []
DEPENDENCIES = []

with open('requirements.txt') as requirements:
    for requirement in requirements.readlines():
        if requirement.startswith('git+git://'):
            DEPENDENCIES.append(requirement)
        else:
            REQUIREMENTS.append(requirement)


setup(
    name='André Duarte',
    projects_urls={
        'Github': 'https://github.com/andrxduarte',
    },
    description='Olá, sou André Duarte, estudante de Ciência da Computação na UFF.',
    long_description=LONG_DESCRIPTION,
    long_description_content_type='text/markdown',
    author=AUTHOR,
    author_email=AUTHOR_EMAIL,
    progammingLanguages=[
        'Python',
        'R',
        'C#',
        'C++',
        'Bash'
    ],
    progammingLanguages_dir={'André'},
    include_progammingLanguages_data=True,
    python_requires='>=3, <=3.11',
    platforms=['any'],
    technologies=[
        'Eclipse for C++/Python',
        'Spyder',
        'Jupyter Notebook',
        'Pycharm',
        'Visual Studio/Code',
        'R Studio',
        'Arduino IDE',
        'Thonny IDE',
    ]
)
