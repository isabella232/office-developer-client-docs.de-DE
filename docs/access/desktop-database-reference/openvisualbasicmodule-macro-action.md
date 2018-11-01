---
title: ÖffnenVisualBasicModul-Makroaktion
TOCTitle: OpenVisualBasicModule Macro Action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bfb2238bf81215acef7026bb878dca9d1dbceb61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869883"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="ee8cc-102">ÖffnenVisualBasicModul-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="ee8cc-102">OpenVisualBasicModule Macro Action</span></span>


<span data-ttu-id="ee8cc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee8cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ee8cc-p101">Sie können die **ÖffnenVisualBasicModul** -Aktion verwenden, um ein angegebenes VBA-Modul (Visual Basic für Applikationen) in einer angegebenen Prozedur zu öffnen. Dies kann eine Unterprozedur, eine Funktion oder eine Ereignisprozedur sein.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ee8cc-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="ee8cc-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ee8cc-108">Setting</span></span>

<span data-ttu-id="ee8cc-109">Die **ÖffnenVisualBasicModul** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-109">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee8cc-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="ee8cc-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ee8cc-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee8cc-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee8cc-112"><strong>Modulname</strong></span><span class="sxs-lookup"><span data-stu-id="ee8cc-112"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ee8cc-113">Der Name des Moduls, den Sie öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-113">The name of the module you want to open.</span></span> <span data-ttu-id="ee8cc-114">Sie können dieses Argument leer lassen, wenn Sie alle Standardmodule in der Datenbank für eine Prozedur durchsuchen, und öffnen Sie das entsprechende Modul bei dieser Prozedur möchten.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-114">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="ee8cc-115">Wenn Sie ein Makro, das die <strong>ÖffnenVisualBasicModul</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Modul mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-115">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee8cc-116"><strong>Prozedurname</strong></span><span class="sxs-lookup"><span data-stu-id="ee8cc-116"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ee8cc-p104">Der Name der Prozedur, in der das Modul geöffnet werden soll. Wenn Sie für dieses Argument keinen Wert eingeben, wird das Modul im Deklarationsbereich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-p104">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="ee8cc-119">[!HINWEIS] Sie müssen entweder im Argument <STRONG>Modulname</STRONG> oder im Argument <STRONG>Prozedurname</STRONG> einen gültigen Namen eingeben.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-119">You must enter a valid name in either the <STRONG>Module Name</STRONG> or <STRONG>Procedure Name</STRONG> argument.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="ee8cc-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee8cc-120">Remarks</span></span>

<span data-ttu-id="ee8cc-121">Diese Aktion können Sie eine Ereignisprozedur öffnen, indem Sie das Argument **Modulname** und im Argument **Prozedurname** angeben.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-121">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="ee8cc-122">Angenommen, Sie zum Öffnen die Ereignisprozedur **Klicken Sie auf** die Schaltfläche Rechnungsdruck auf dem Formular Bestellungen das Argument **Modulname** auf **Form.Orders** festgelegt und die für das Argument **Prozedurname** festlegen **Rechnungsdruck\_klicken Sie auf**.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-122">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="ee8cc-123">Wenn die Ereignisprozedur für ein Formular oder Bericht anzeigen möchten, muss das Formular oder der Bericht geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-123">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="ee8cc-124">Zum Öffnen einer Prozedur in einem Klassenmodul müssen Sie den Modulnamen entsprechend festlegen, obwohl das Klassenmodul nicht geöffnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-124">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="ee8cc-125">Zum Öffnen einer privaten Prozedur muss das Modul, in dem diese Prozedur enthalten ist, geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-125">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="ee8cc-p106">Diese Aktion bewirkt dasselbe, wie wenn Sie im Navigationsbereich auf ein Modul doppelklicken und dann auf **Entwurfsansicht** klicken. Mithilfe dieser Aktion können Sie außerdem einen Prozedurnamen angeben und in den Standardmodulen in einer Datenbank nach Prozeduren suchen.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-p106">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>


> [!TIP]
> <P><span data-ttu-id="ee8cc-p107">[!TIPP] Sie können ein Modul im Navigationsbereich auswählen und in die Aktionszeile des Makros ziehen. Damit wird automatisch eine <STRONG>ÖffnenVisualBasicModul</STRONG> -Aktion erstellt, mit der das Modul im Deklarationsbereich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-p107">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an <STRONG>OpenVisualBasicModule</STRONG> action that opens the module to the Declarations section.</span></span></P>



<span data-ttu-id="ee8cc-130">Wenn Sie die **ÖffnenVisualBasicModul** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) ausführen möchten, verwenden Sie die **OpenModule** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ee8cc-130">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

