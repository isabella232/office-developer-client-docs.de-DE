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
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306521"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="fc32c-102">SetTempVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="fc32c-102">SetTempVar macro action</span></span>


<span data-ttu-id="fc32c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc32c-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="fc32c-p101">Sie können die **FestlegenTempVar**-Aktion verwenden, um eine temporäre Variable zu erstellen und auf einen bestimmten Wert festzulegen. Die Variable kann dann als Bedingung oder Argument in nachfolgenden Aktionen verwendet werden. Sie können die Variable auch in einem anderen Makro, in einer Ereignisprozedur oder in einem Formular bzw. Bericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc32c-p101">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="fc32c-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="fc32c-106">Setting</span></span>

<span data-ttu-id="fc32c-107">Die **FestlegenTempVar** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="fc32c-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc32c-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="fc32c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fc32c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc32c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc32c-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="fc32c-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fc32c-111">Geben Sie den Namen der temporären Variable ein.</span><span class="sxs-lookup"><span data-stu-id="fc32c-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc32c-112"><strong>Ausdruck</strong></span><span class="sxs-lookup"><span data-stu-id="fc32c-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="fc32c-113">Geben Sie einen Ausdruck ein, der zum Festlegen des Werts für diese temporäre Variable verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc32c-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="fc32c-114">Stellen Sie dem Ausdruck nicht das Gleichheitszeichen (<strong>=</strong>) voran.</span><span class="sxs-lookup"><span data-stu-id="fc32c-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="fc32c-115">Sie können auf die <strong>Generator</strong> -Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="fc32c-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="fc32c-117">Verwenden Sie zum Festlegen dieses Arguments den Ausdrucks-Generator.</span><span class="sxs-lookup"><span data-stu-id="fc32c-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fc32c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc32c-118">Remarks</span></span>

- <span data-ttu-id="fc32c-p103">Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Eine temporäre Variable, die Sie nicht entfernen, verbleibt bis zum Schließen der Datenbank im Speicher. Es empfiehlt sich, temporäre Variablen zu entfernen, die nicht mehr benötigt werden. Wenn Sie eine einzelne temporäre Variable entfernen möchten, verwenden Sie die **[EntfernenTempVar](removetempvar-macro-action.md)** -Aktion. Legen Sie deren Argument auf den Namen der temporären Variable fest, die entfernt werden soll. Falls Sie mit mehreren temporären Variablen arbeiten und alle gleichzeitig entfernen möchten, verwenden Sie die **EntfernenAlleTempVar** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="fc32c-p103">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them. To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove. If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="fc32c-124">Temporäre Variablen sind Global.</span><span class="sxs-lookup"><span data-stu-id="fc32c-124">Temporary variables are global.</span></span> <span data-ttu-id="fc32c-125">Nachdem eine temporäre Variable erstellt wurde, können Sie in einer Ereignisprozedur, einem VBA-Modul (Visual Basic für Applikationen), einer Abfrage oder einem Ausdruck darauf verweisen.</span><span class="sxs-lookup"><span data-stu-id="fc32c-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="fc32c-126">Wenn Sie beispielsweise eine temporäre Variable mit dem Namen *MeineVar*erstellt haben, können Sie die Variable als Steuerelementquelle für ein Textfeld mithilfe der folgenden Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="fc32c-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="fc32c-127">[!HINWEIS] In Makros, Abfragen und Ereignisprozeduren müssen Sie dem Ausdruck kein Gleichheitszeichen voranstellen.</span><span class="sxs-lookup"><span data-stu-id="fc32c-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="fc32c-128">Sie können in allen Add-Ins und referenzierten Datenbanken auf temporäre Variablen verweisen.</span><span class="sxs-lookup"><span data-stu-id="fc32c-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="fc32c-129">Wenn Sie die **FestlegenTempVar** -Aktion in einem VBA-Modul ausführen möchten, verwenden Sie die **Add** -Methode des Objekts **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="fc32c-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="fc32c-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fc32c-130">Example</span></span>

<span data-ttu-id="fc32c-131">Das folgende Makro veranschaulicht, wie Sie mithilfe der **FestlegenTempVar** -Aktion eine temporäre Variable erstellen, diese dann in einer Bedingung und einem Meldungsfeld verwenden und sie anschließend entfernen.</span><span class="sxs-lookup"><span data-stu-id="fc32c-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc32c-132">Bedingung</span><span class="sxs-lookup"><span data-stu-id="fc32c-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="fc32c-133">Aktion</span><span class="sxs-lookup"><span data-stu-id="fc32c-133">Action</span></span></p></th>
<th><p><span data-ttu-id="fc32c-134">Argumente</span><span class="sxs-lookup"><span data-stu-id="fc32c-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fc32c-135"><strong>FestlegenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="fc32c-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="fc32c-136"><strong>Name</strong>: MeineVar<strong>Ausdruck</strong>: InputBox (&quot;geben Sie eine Zahl ungleich NULL&quot;ein.)</span><span class="sxs-lookup"><span data-stu-id="fc32c-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc32c-137">[TempVars]! MeineVar &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="fc32c-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="fc32c-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="fc32c-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="fc32c-139"><strong>Meldung</strong>: =&quot;Sie haben &quot; &amp; [TempVars] eingegeben! MeineVar &amp; &quot;. &quot; <strong>Beep</strong>: <strong>jatyp</strong>: <strong>Informationen</strong></span><span class="sxs-lookup"><span data-stu-id="fc32c-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fc32c-140"><strong>EntfernenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="fc32c-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="fc32c-141"><strong>Name</strong>: MeineVar</span><span class="sxs-lookup"><span data-stu-id="fc32c-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

