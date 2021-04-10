.. include:: /Includes.rst.txt
.. _tca_property_fieldWizard_localizationStateSelector:

=========================
localizationStateSelector
=========================

.. confval:: localizationStateSelector

   :type: array
   :Scope: fieldWizard

   :Types: :ref:`check <columns-check>`, :ref:`flex <columns-flex>`,
      :ref:`group <columns-group>`,
      :ref:`imageManipulation <columns-imageManipulation>`,
      :ref:`input <columns-input>`

   The localization state selector wizard displays two or three radio buttons
   in localized records saying: "Custom value", "This field
   has the same value as the default language record" or
   "Value of default language". If the latter value is chosen the field is
   displayed read-only.

   It will only render, if:

   *  The record is a localized record (not default language)
   *  The record is in "translated" (connected), but not in "copy" (free) mode
   *  The table is localization aware using the ['ctrl'] properties
      :ref:`languageField <ctrl-reference-languagefield>`,
      :ref:`transOrigPointerField <ctrl-reference-transorigpointerfield>`.
   *  The property ['config']['behaviour']['allowLanguageSynchronization']
      is set to true

   If the optional property
   :ref:`translationSource <ctrl-reference-translationSource>` is also set, and
   if the record is a translation from another localized record, the third
   radio appears.


Example
=======

Localization state selector on a `type=input` field:

.. include:: /Includes/Images/Styleguide/RstIncludes/TranslatedInput1.rst.txt

The same field in a language that has been translated from another language:

.. include:: /Includes/Images/Styleguide/RstIncludes/FrenchInput1.rst.txt

The TCA definition:

.. include:: /Includes/Images/Styleguide/RstIncludes/Input1.rst.txt
