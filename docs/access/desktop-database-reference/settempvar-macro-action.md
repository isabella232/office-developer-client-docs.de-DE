---
title: SetTempVar-Makroaktion
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 342a4db4e2ed6e06dca917beb96b4562f1fc65da
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919444"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="3f54d-102">SetTempVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="3f54d-102">SetTempVar macro action</span></span>


<span data-ttu-id="3f54d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f54d-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="3f54d-p101">Sie können die **FestlegenTempVar** -Aktion verwenden, um eine temporäre Variable zu erstellen und auf einen bestimmten Wert festzulegen. Die Variable kann dann als Bedingung oder Argument in nachfolgenden Aktionen verwendet werden. Sie können die Variable auch in einem anderen Makro, in einer Ereignisprozedur oder in einem Formular bzw. Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f54d-p101">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="3f54d-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3f54d-106">Setting</span></span>

<span data-ttu-id="3f54d-107">Die **FestlegenTempVar** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="3f54d-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f54d-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="3f54d-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3f54d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f54d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f54d-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="3f54d-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3f54d-111">Geben Sie den Namen der temporären Variable ein.</span><span class="sxs-lookup"><span data-stu-id="3f54d-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f54d-112"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="3f54d-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="3f54d-113">Geben Sie einen Ausdruck, der verwendet wird, um den Wert für diese temporäre Variable festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3f54d-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="3f54d-114">Setzen Sie den Ausdruck mit dem Gleichheitszeichen (<strong>=</strong>) anmelden.</span><span class="sxs-lookup"><span data-stu-id="3f54d-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="3f54d-115">Klicken Sie auf die <strong>Generator</strong> -Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="3f54d-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="3f54d-117">, um das Argument mithilfe des Ausdrucks-Generators festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3f54d-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3f54d-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f54d-118">Remarks</span></span>

- <span data-ttu-id="3f54d-p103">Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Eine temporäre Variable, die Sie nicht entfernen, verbleibt bis zum Schließen der Datenbank im Speicher. Es empfiehlt sich, temporäre Variablen zu entfernen, die nicht mehr benötigt werden. Wenn Sie eine einzelne temporäre Variable entfernen möchten, verwenden Sie die **[EntfernenTempVar](removetempvar-macro-action.md)** -Aktion. Legen Sie deren Argument auf den Namen der temporären Variable fest, die entfernt werden soll. Falls Sie mit mehreren temporären Variablen arbeiten und alle gleichzeitig entfernen möchten, verwenden Sie die **EntfernenAlleTempVar** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="3f54d-p103">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them. To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove. If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="3f54d-124">Temporäre Variablen sind global.</span><span class="sxs-lookup"><span data-stu-id="3f54d-124">Temporary variables are global.</span></span> <span data-ttu-id="3f54d-125">Nachdem eine temporäre Variable erstellt wurde, können Sie es in einer Ereignisprozedur einem Visual Basic für Applikationen (VBA) Modul, einer Abfrage oder einem Ausdruck verweisen.</span><span class="sxs-lookup"><span data-stu-id="3f54d-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="3f54d-126">Angenommen, wenn Sie eine temporäre Variable mit dem Namen *Meinevar*erstellt, können die Variable als Steuerelementinhalt für ein Textfeld Sie mithilfe der folgenden Syntax:</span><span class="sxs-lookup"><span data-stu-id="3f54d-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="3f54d-127">[!HINWEIS] In Makros, Abfragen und Ereignisprozeduren müssen Sie dem Ausdruck kein Gleichheitszeichen voranstellen.</span><span class="sxs-lookup"><span data-stu-id="3f54d-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="3f54d-128">Sie können in allen Add-Ins und referenzierten Datenbanken auf temporäre Variablen verweisen.</span><span class="sxs-lookup"><span data-stu-id="3f54d-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="3f54d-129">Wenn Sie die **FestlegenTempVar** -Aktion in einem VBA-Modul ausführen möchten, verwenden Sie die **Add** -Methode des Objekts **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="3f54d-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="3f54d-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f54d-130">Example</span></span>

<span data-ttu-id="3f54d-131">Das folgende Makro veranschaulicht, wie Sie mithilfe der **FestlegenTempVar** -Aktion eine temporäre Variable erstellen, diese dann in einer Bedingung und einem Meldungsfeld verwenden und sie anschließend entfernen.</span><span class="sxs-lookup"><span data-stu-id="3f54d-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f54d-132">Bedingung</span><span class="sxs-lookup"><span data-stu-id="3f54d-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="3f54d-133">Aktion</span><span class="sxs-lookup"><span data-stu-id="3f54d-133">Action</span></span></p></th>
<th><p><span data-ttu-id="3f54d-134">Argumente</span><span class="sxs-lookup"><span data-stu-id="3f54d-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="3f54d-135"><strong>FestlegenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="3f54d-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="3f54d-136"><strong>Name</strong>: Meinevar<strong>Ausdruck</strong>: InputBox (&quot;Geben Sie eine Zahl ungleich NULL.&quot;)</span><span class="sxs-lookup"><span data-stu-id="3f54d-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f54d-137">[TempVars]! [Meinevar] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="3f54d-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="3f54d-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="3f54d-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="3f54d-139"><strong>Meldung</strong>: =&quot;eingegebene &quot; &amp; [TempVars]! [Meinevar] &amp; &quot;. &quot; <strong>Signalton</strong>: <strong>YesType</strong>: <strong>Informationen</strong></span><span class="sxs-lookup"><span data-stu-id="3f54d-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="3f54d-140"><strong>EntfernenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="3f54d-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="3f54d-141"><strong>Name</strong>: MeineVar</span><span class="sxs-lookup"><span data-stu-id="3f54d-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

