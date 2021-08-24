$("body").on("click", ".select_color", function ()
    {
        if ($(this).hasClass("iscolor"))
        {
            $(this).removeClass("iscolor");
        } else
        {
            $(this).addClass("iscolor");
        }
        var value = {};
        $(this)
            .parent()
            .find(".select_color.iscolor")
            .each(function (index, el)
            {
                value[index] = $(el).attr("data-code");
            });

        var data = {};
        data.value = value;
        data.id = $(this)
            .parents("tr")
            .attr("data-id");
        data.code = "COLOR_IMAGE";
        code = "edit_one";

        $.ajax({
            url: "/local/components/cod/pro/ajax.php",
            type: "POST",
            data: { data: data, code: code }
        }).done(function () { });
    });
