# jQuery Tagify Customized

Added my options to jQuery.Tagify by Alicia Liu.

https://github.com/alicial/jQuery.Tagify

* Replacing remove button's HTML fragment
* Flag to serialize immediately
* onCreate and onChange callback

# Usage

<pre>
$('textarea').tagify({

    // Replace close button 'x' to 'close'
    removeButton: 'close',

    // Serialize immediately on changed tags
    serializeImmediately: true,

    // Callback after create widget
    onCreate: function() {
        // For example, add an anchor after new tag textbox
        var widget = this;
        var $a = $('<a href="#">alert</a>').click(function() {
            alert($(widget.element).val());
        });
        this.tagInput.after($a);
    },

    // Callback on changed tags - Adding and removing
    // * Using onChange is the same as serializeImmediately: true.
    onChange: function(newValue) {
        alert('tags changed to ' + newValue);
    }
});
</pre>
