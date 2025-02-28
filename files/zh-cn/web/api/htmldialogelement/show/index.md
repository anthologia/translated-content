---
title: HTMLDialogElement.show()
slug: Web/API/HTMLDialogElement/show
---

{{ APIRef("HTML DOM") }} {{ SeeCompatTable() }}

The **`show()`** method of the {{domxref("HTMLDialogElement")}} interface displays the dialog modelessly, i.e. still allowing interaction with content outside of the dialog.

## Syntax

```plain
dialogInstance.show();
```

### Parameters

None.

### Return value

Void.

## Examples

The following example shows a simple button that, when clicked, opens a {{htmlelement("dialog")}} containing a form via the `show()` method. From there you can click the _Cancel_ button to close the dialog (via the {{domxref("HTMLDialogElement.close()")}} method), or submit the form via the submit button.

```html
  <!-- Simple pop-up dialog box, containing a form -->
  <dialog id="favDialog">
    <form method="dialog">
      <section>
        <p><label for="favAnimal">Favorite animal:</label>
        <select id="favAnimal" name="favAnimal">
          <option></option>
          <option>Brine shrimp</option>
          <option>Red panda</option>
          <option>Spider monkey</option>
        </select></p>
      </section>
      <menu>
        <button id="cancel" type="reset">Cancel</button>
        <button type="submit">Confirm</button>
      </menu>
    </form>
  </dialog>

  <menu>
    <button id="updateDetails">Update details</button>
  </menu>

  <script>
    (function() {
      var updateButton = document.getElementById('updateDetails');
      var cancelButton = document.getElementById('cancel');
      var dialog = document.getElementById('favDialog');
      dialog.returnValue = 'favAnimal';

      function openCheck(dialog) {
        if(dialog.open) {
          console.log('Dialog open');
        } else {
          console.log('Dialog closed');
        }
      }

      // Update button opens a modal dialog
      updateButton.addEventListener('click', function() {
        dialog.showModal();
        openCheck(dialog);
      });

      // Form cancel button closes the dialog box
      cancelButton.addEventListener('click', function() {
        dialog.close('animalNotChosen');
        openCheck(dialog);
      });

    })();
  </script>
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat("api.HTMLDialogElement.show")}}

## See also

- The HTML element implementing this interface: {{ HTMLElement("dialog") }}.
