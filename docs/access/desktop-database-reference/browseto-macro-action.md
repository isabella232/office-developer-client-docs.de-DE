---
title: BrowseTo-Makroaktion
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c648e7ea8700a6881e3cc2deda4fd2ee9955c8b1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923811"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="8b2e0-102">BrowseTo-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="8b2e0-102">BrowseTo macro action</span></span>

<span data-ttu-id="8b2e0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b2e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b2e0-p101">Mit der **WechselnZu** -Aktion können Sie zwischen Objekten an ihrem Ort wechseln. Zudem können Sie das Quellobjekt eines Unterformular-Steuerelements ändern, indem Sie das Argument Path to Subform Control angeben. Verwenden Sie **WechselnZu**, um von Formular1 zu Formular2 zu wechseln, ohne ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="8b2e0-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="8b2e0-107">Setting</span></span>

<span data-ttu-id="8b2e0-108">Die **WechselnZu** -Aktion wird mit den folgenden Argumenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b2e0-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="8b2e0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8b2e0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b2e0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b2e0-111">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="8b2e0-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="8b2e0-112">Der Typ des Objekts, zu dem gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b2e0-113">Objektname</span><span class="sxs-lookup"><span data-stu-id="8b2e0-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="8b2e0-114">Das Objekt, das in dem Unterformular-Steuerelement geladen wird, auf das das Argument Pfad zu Unterformular-Steuerelement verweist.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b2e0-115">Pfad zu Unterformular-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8b2e0-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="8b2e0-116">Wenn angegeben, der Pfad vom Hauptformular der Anwendung zum Unterformular steuern, lädt das Objekt, das durch das Argument Objektname angegeben.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b2e0-117">Where Condition</span><span class="sxs-lookup"><span data-stu-id="8b2e0-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="8b2e0-118">Ersetzt, wenn angegeben, die Bedingung der Datensatzquelle des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b2e0-119">Page</span><span class="sxs-lookup"><span data-stu-id="8b2e0-119">Page</span></span></p></td>
<td><p><span data-ttu-id="8b2e0-120">Legt, wenn angegeben, die Seite des Endlosformulars fest, die als aktuelle Seite festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="8b2e0-121">Dieses Argument ist nur Web.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b2e0-122">Data Mode</span><span class="sxs-lookup"><span data-stu-id="8b2e0-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="8b2e0-123">Wenn angegeben, der Dateneingabemodus des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8b2e0-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b2e0-124">Remarks</span></span>

<span data-ttu-id="8b2e0-125">Das Argument PathToSubFormControl muss mit der Syntax im folgenden Codebeispiel wird angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="8b2e0-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="8b2e0-126">In diesem Beispiel bildet das Hauptformular in der Access-Clientanwendung das Formular der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-126">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="8b2e0-127">Der Pfad zum Formularsteuerelement Sub-Argument muss auch angeben und Unterformular Steuerelementnamen führende aus dem Hauptformular auf das Unterformular-Steuerelement, das den Container des Objekts, das durch das Argument Objektname angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-127">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="8b2e0-128">Jedes angegebene Unterformular-Steuerelement muss ein Steuerelement für das Formular darstellen, das ihm vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-128">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="8b2e0-129">Der Pfad muss mit einem Unterformular-Steuerelement enden.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-129">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="8b2e0-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8b2e0-130">Example</span></span>

<span data-ttu-id="8b2e0-131">Das folgende Beispiel zeigt, wie Sie die BrowseTo-Aktion zum Öffnen eines Berichts in einem Unterformular-Steuerelement oder in einem Navigationssteuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b2e0-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="8b2e0-132">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8b2e0-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



