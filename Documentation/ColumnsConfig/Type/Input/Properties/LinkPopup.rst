.. include:: /Includes.rst.txt
.. _tca_property_fieldControl_linkPopup:

.. _tca_field_control_link_popup:

=========
linkPopup
=========

.. confval:: linkPopup

   :type: array
   :Scope: fieldControl
   :RenderTypes: inputLink

   The link browser control is typically used with `type='input'` with `renderType='inputLink'` adding a button
   which opens a modal to select an internal link to a page, an external link or a mail address.

   **Options:**

   pid (string)
      pid of the new record. Can be a hard pid setting, or one of these markers, see
      :ref:`select foreign_table_where <columns-select-properties-foreign-table-where>`.
      Falls back to "current pid" if not set, forces pid=0 if records of this table are only
      allowed on root level.

      - :code:`###CURRENT_PID###`
      - :code:`###THIS_UID###`
      - :code:`###SITEROOT###`

   allowedExtensions (string, list)
      Comma separated list of allowed file extensions. By default, all extensions are allowed.

   blindLinkFields (string, list)
      Comma separated list of link fields that should not be displayed. Possible values are
      `class`, `params`, `target` and `title`. By default, all link fields are displayed.

   blindLinkOptions (string, list)
      Comma separated list of link options that should not be displayed. Possible values are
      `file`, `folder`, `mail`, `page`, `spec`, `telephone` and `url`. By default, all link options are displayed.

   title (string or LLL reference)
      Allows to set a different 'title' attribute to the popup icon, defaults
      to :code:`LLL:EXT:lang/Resources/Private/Language/locallang_core.xlf:labels.link`
