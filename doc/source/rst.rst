=====================
Understanding the RST
=====================

If you want to edit OTC documentation you need to edit it using restructuredtext. 
The basics of RST will be covered in this documentation. 

Integrating Images
==================

If you simply want to implement a picture you can use following syntax:

    .. code-block:: 
        
        |imagexx|

       .. |imagexx| image:: /_static/images/filename

   .. note:: This is an easy way to implement pictures espacially in tables. Ideally the file path would be at the bottom of your file. 

The more elegant way is to use figures with following syntax:

    .. code-block:: 

        .. figure:: /_static/images/filename

            :alt: This is your title 



Integrating Admonitions 
=======================

restructuredtext has ten standard admonitions and one generic. 
If you want to raise awereness or hint to something you can use following Admonitions:

        - attention

        - caution

        - danger

        - error

        - hint

        - important

        - note

        - tip

        - warning

        - admonition

        - seealso

Using following syntax these admonitions can be implemented: 

    .. code-block::

        .. note::

            This is a note

    


You can use an generic admonition with following syntax:

    .. code-block::

        .. admonition:: generic admonition title

            generic admonition content 

    
    
Integrating Tables
==================



toctree
=======

Restructuredtext does not offer any way to interconnect multiple files or split one file up. 
Therefore, sphinx uses a custom directive called toctree to add relations between documents. 
Also toctree is used for tables of content. 

The maxdepth function is used to limit the depth. 
This helps to improve navigability of the resulting page. 
As a best practice we agreed on **x** on maxdepth. 

As an example the index.rst file of this site: 

    .. code-block::

        ..toctree::
            :maxdepth: 1


                structure
                change_proposal_process
                reviewer
                approver
                git_account
                code_editors
                rst
                migration
                presentations/index

    

Markdown + RST
==============

Markdown and RST both are lightweight markup languages that empathize plain text readabilty. 

Markdown is mainly used to be formated for the web and it supports inline html

Restructuredtext is used in technical documentation like this documentation. 


Useful Links
============
https://www.sphinx-doc.org/en/master/usage/restructuredtext/

https://restructuredtext.documatt.com/

https://www.sphinx-doc.org/en/1.0/markup/toctree.html

https://www.zverovich.net/2016/06/16/rst-vs-markdown.html
