.. include:: ../README.rst

----

Sphinx configuration file used to build these here docs (:doc:`see full file <conf>`),

This branch shows a proof of concept for visual diff between two rendered
versions. To try this locally, do something like:

.. code:: console

    % rm -rf docs/_build
    % git checkout main
    % cd docs/
    % sphinx-build -Eb html . _build/main
    % git checkout visual-diff
    % sphinx-build -Eb html . _build/pr
    % cd _build
    % python -m http.server 8080

Then open your browser at http://127.0.0.1:8080/pr/

.. literalinclude:: conf.py
   :language: python
   :end-before: ###########################################################################
   :linenos:

----

.. runblock:: pycon

   >>> # Build at
   >>> import datetime
   >>> datetime.datetime.utcnow()  # UTC
