Emoji
=====
Emoji for Python. This project was inspired by kyokomi.


BUILDING STATUS:
----------
.. image:: https://travis-ci.com/Eloypripan/emoji.svg?branch=master
    :target: https://travis-ci.com/Eloypripan/emoji


Example
-------

The entire set of Emoji codes as defined by the `unicode consortium <http://www.unicode.org/Public/emoji/1.0/full-emoji-list.html>`__
is supported in addition to a bunch of `aliases <http://www.emoji-cheat-sheet.com/>`__.  By
default only the official list is enabled but doing ``emoji.emojize(use_aliases=True)`` enables
both the full list and aliases.

.. code-block:: python

    >> import emoji
    >> print(emoji.emojize('Python is :thumbs_up:'))
    Python is 👍
    >> print(emoji.emojize('Python is :thumbsup:', use_aliases=True))
    Python is 👍
    >> print(emoji.demojize('Python is 👍'))
    Python is :thumbs_up:
    
    >> botcid = m.chat.id
    >> bot.send_message(cid, emoji.emojize('Bot is :thumbsup:')
    Bot is 👍

Installation
------------

Via pip:

.. code-block:: console

    $ pip install emoji --upgrade

From master branch:

.. code-block:: console

    $ git clone https://github.com/Eloypripan/emoji.git
    $ cd emoji
    $ python setup.py install


Developing
----------

.. code-block:: console

    $ git clone https://github.com/Eloypripan/emoji.git
    $ cd emoji
    $ pip install -e .\[dev\]
    $ nosetests

The ``utils/get-codes-from-unicode-consortium.py`` may help when updating
``unicode_codes.py`` but is not guaranteed to work.  Generally speaking it
scrapes a table on the Unicode Consortium's website with
`BeautifulSoup <http://www.crummy.com/software/BeautifulSoup/>`_ and prints the
contents to ``stdout`` in a more useful format.


Link
----

`Emoji Cheat Sheet <http://www.emoji-cheat-sheet.com/>`__

`Official unicode list <http://www.unicode.org/Public/emoji/1.0/full-emoji-list.html>`__


Authors
------- 
Updated in Jan 2019 by Eloy Prieto / `@Eloypripan <http://github.com/Eloypripan/>`__

Initial proyect from 2004-2005

Taehoon Kim / `@carpedm20 <http://carpedm20.github.io/about/>`__

Kevin Wurster / `@geowurster <http://twitter.com/geowurster/>`__
