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
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296773"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="07f4c-102">BrowseTo-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="07f4c-102">BrowseTo macro action</span></span>

<span data-ttu-id="07f4c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07f4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07f4c-104">Mit der **WechselnZu** -Aktion können Sie zwischen Objekten an ihrem Ort wechseln.</span><span class="sxs-lookup"><span data-stu-id="07f4c-104">You can use the **BrowseTo** action to navigate between objects in place.</span></span> <span data-ttu-id="07f4c-105">Zudem können Sie das Quellobjekt eines Unterformular-Steuerelements ändern, indem Sie das Argument Path to Subform Control angeben.</span><span class="sxs-lookup"><span data-stu-id="07f4c-105">You can also change the source object of a subform control by specifying the Path to Subform Control argument.</span></span> <span data-ttu-id="07f4c-106">Verwenden Sie **WechselnZu**, um von Formular1 zu Formular2 zu wechseln, ohne ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="07f4c-106">Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="07f4c-107">Einstellung</span><span class="sxs-lookup"><span data-stu-id="07f4c-107">Setting</span></span>

<span data-ttu-id="07f4c-108">Die **WechselnZu**-Aktion wird mit den folgenden Argumenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="07f4c-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07f4c-109">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="07f4c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="07f4c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07f4c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07f4c-111">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="07f4c-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="07f4c-112">Der Objekttyp, zu dem navigiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07f4c-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f4c-113">Objektname</span><span class="sxs-lookup"><span data-stu-id="07f4c-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="07f4c-114">Das Objekt, das in dem Unterformular-Steuerelement geladen wird, auf das durch das Argument path to Subform Control verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="07f4c-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07f4c-115">Path to Subform Control</span><span class="sxs-lookup"><span data-stu-id="07f4c-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="07f4c-116">Wenn angegeben, der Pfad vom Hauptformular der Anwendung zum Ziel Unterformular-Steuerelement, das das durch das Argument Object Name angegebene Objekt lädt.</span><span class="sxs-lookup"><span data-stu-id="07f4c-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f4c-117">Bedingung</span><span class="sxs-lookup"><span data-stu-id="07f4c-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="07f4c-118">Ersetzt die WHERE-Bedingung (sofern angegeben) der Objektdatenquelle.</span><span class="sxs-lookup"><span data-stu-id="07f4c-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07f4c-119">Seite</span><span class="sxs-lookup"><span data-stu-id="07f4c-119">Page</span></span></p></td>
<td><p><span data-ttu-id="07f4c-120">Legt die Seite des Endlosformulars fest, die als aktuelle Seite bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="07f4c-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="07f4c-121">Dieses Argument ist nur Web.</span><span class="sxs-lookup"><span data-stu-id="07f4c-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07f4c-122">Datenmodus</span><span class="sxs-lookup"><span data-stu-id="07f4c-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="07f4c-123">Der Dateneingabemodus des Formulars (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="07f4c-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="07f4c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07f4c-124">Remarks</span></span>

<span data-ttu-id="07f4c-125">Das Argument PathToSubFormControl muss mit der Syntax im folgenden Codebeispiel angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="07f4c-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="07f4c-126">In this example, the Main Form is the top level form in the Access client application.</span><span class="sxs-lookup"><span data-stu-id="07f4c-126">In this example, the Main Form is the top level form in the Access client application.</span></span> <span data-ttu-id="07f4c-127">Das Argument path to Sub Form Control muss die Namen von Formular-und subformular-Steuerelementen, die vom Hauptformular zum Unterformular-Steuerelement führen, als Container des durch das Argument Object Name angegebenen Objekts angeben.</span><span class="sxs-lookup"><span data-stu-id="07f4c-127">The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument.</span></span> <span data-ttu-id="07f4c-128">Each subform control specified must be a control on the form that precedes it.</span><span class="sxs-lookup"><span data-stu-id="07f4c-128">Each subform control specified must be a control on the form that precedes it.</span></span> <span data-ttu-id="07f4c-129">Der Pfad muss mit einem Unterformular-Steuerelement enden.</span><span class="sxs-lookup"><span data-stu-id="07f4c-129">The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="07f4c-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="07f4c-130">Example</span></span>

<span data-ttu-id="07f4c-131">Das folgende Beispiel zeigt, wie Sie die BrowseTo-Aktion zum Öffnen eines Berichts in einem Unterformular-Steuerelement oder in einem Navigationssteuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f4c-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="07f4c-132">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="07f4c-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



