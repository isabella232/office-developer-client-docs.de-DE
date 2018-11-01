---
title: WechselnZu-Makroaktion
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 242041627a909b1c16d956dbbb94a3bf173d544a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878934"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="ad823-102">WechselnZu-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="ad823-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="ad823-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad823-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad823-p101">Mit der **WechselnZu** -Aktion können Sie zwischen Objekten an ihrem Ort wechseln. Zudem können Sie das Quellobjekt eines Unterformular-Steuerelements ändern, indem Sie das Argument Path to Subform Control angeben. Verwenden Sie **WechselnZu**, um von Formular1 zu Formular2 zu wechseln, ohne ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad823-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="ad823-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ad823-107">Setting</span></span>

<span data-ttu-id="ad823-108">Die **WechselnZu** -Aktion wird mit den folgenden Argumenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad823-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad823-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="ad823-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ad823-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad823-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad823-111">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="ad823-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="ad823-112">Der Typ des Objekts, zu dem gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad823-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad823-113">Objektname</span><span class="sxs-lookup"><span data-stu-id="ad823-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="ad823-114">Das Objekt, das in dem Unterformular-Steuerelement geladen wird, auf das das Argument Pfad zu Unterformular-Steuerelement verweist.</span><span class="sxs-lookup"><span data-stu-id="ad823-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad823-115">Pfad zu Unterformular-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad823-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="ad823-116">Wenn angegeben, der Pfad vom Hauptformular der Anwendung zum Unterformular steuern, lädt das Objekt, das durch das Argument Objektname angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad823-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad823-117">Where Condition</span><span class="sxs-lookup"><span data-stu-id="ad823-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="ad823-118">Ersetzt, wenn angegeben, die Bedingung der Datensatzquelle des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ad823-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad823-119">Page</span><span class="sxs-lookup"><span data-stu-id="ad823-119">Page</span></span></p></td>
<td><p><span data-ttu-id="ad823-120">Legt, wenn angegeben, die Seite des Endlosformulars fest, die als aktuelle Seite festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ad823-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="ad823-121">Dieses Argument ist nur Web.</span><span class="sxs-lookup"><span data-stu-id="ad823-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad823-122">Data Mode</span><span class="sxs-lookup"><span data-stu-id="ad823-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="ad823-123">Wenn angegeben, der Dateneingabemodus des Formulars.</span><span class="sxs-lookup"><span data-stu-id="ad823-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ad823-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad823-124">Remarks</span></span>

<span data-ttu-id="ad823-125">Das Argument PathToSubFormControl muss mit der Syntax im folgenden Codebeispiel wird angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="ad823-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="ad823-126">In diesem Beispiel bildet das Hauptformular in der Access-Clientanwendung das Formular der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="ad823-126">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="ad823-127">Der Pfad zum Formularsteuerelement Sub-Argument muss auch angeben und Unterformular Steuerelementnamen führende aus dem Hauptformular auf das Unterformular-Steuerelement, das den Container des Objekts, das durch das Argument Objektname angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ad823-127">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="ad823-128">Jedes angegebene Unterformular-Steuerelement muss ein Steuerelement für das Formular darstellen, das ihm vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="ad823-128">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="ad823-129">Der Pfad muss mit einem Unterformular-Steuerelement enden.</span><span class="sxs-lookup"><span data-stu-id="ad823-129">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="ad823-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ad823-130">Example</span></span>

<span data-ttu-id="ad823-131">Das folgende Beispiel zeigt, wie Sie die BrowseTo-Aktion zum Öffnen eines Berichts in einem Unterformular-Steuerelement oder in einem Navigationssteuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad823-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="ad823-132">**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ad823-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



