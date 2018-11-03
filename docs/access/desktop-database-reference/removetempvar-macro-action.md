---
title: RemoveTempVar-Makroaktion
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e43181626b885664eaf370decb7d471082c7a263
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928117"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="5e1b2-102">RemoveTempVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="5e1b2-102">RemoveTempVar macro action</span></span>


<span data-ttu-id="5e1b2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e1b2-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="5e1b2-104">Mit der **EntfernenTempVar** -Aktion können Sie eine einzelne mit der **FestlegenTempVar** -Aktion erstellte temporäre Variable entfernen.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="5e1b2-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="5e1b2-105">Setting</span></span>

<span data-ttu-id="5e1b2-106">Die **EntfernenTempVar** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e1b2-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="5e1b2-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5e1b2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e1b2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e1b2-109"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="5e1b2-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5e1b2-110">Geben Sie den Namen der zu entfernenden temporären Variable ein.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5e1b2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e1b2-111">Remarks</span></span>

  - <span data-ttu-id="5e1b2-p101">Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Wenn eine temporäre Variable nicht entfernt wird, verbleibt diese bis zum Schließen der Datenbank im Arbeitsspeicher. Es empfiehlt sich, temporäre Variablen zu entfernen, sobald Sie deren Verwendung beendet haben.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="5e1b2-115">Beim Schließen der Datenbank oder des Projekts werden von Access automatisch alle temporären Variablen entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="5e1b2-p102">Wenn der Name der zu entfernenden Variable falsch geschrieben wird, wird von Access kein Fehler angezeigt. Die zu entfernende Variable verbleibt bis zum Schließen der Datenbank im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-p102">If you misspell the name of the variable to be removed, Access does not display an error. The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="5e1b2-118">Wenn Sie mehr als eine temporäre Variable erstellt haben und alle gleichzeitig entfernt werden sollen, verwenden Sie die **EntfernenAlleTempVar** -Aktion.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="5e1b2-119">Verwenden Sie zum Ausführen der **EntfernenTempVar** -Aktion in einem VBA-Modul die **Remove** -Methode des **TempVars** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="5e1b2-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5e1b2-120">Example</span></span>

<span data-ttu-id="5e1b2-121">Im folgenden Makro wird die Vorgehensweise zum Erstellen einer temporären Variable, zum Verwenden der Variable in einer Bedingung und einem Meldungsfeld und zum anschließenden Entfernen der temporären Variable mit der **EntfernenTempVar** -Aktion gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5e1b2-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e1b2-122">Bedingung</span><span class="sxs-lookup"><span data-stu-id="5e1b2-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="5e1b2-123">Aktion</span><span class="sxs-lookup"><span data-stu-id="5e1b2-123">Action</span></span></p></th>
<th><p><span data-ttu-id="5e1b2-124">Argumente</span><span class="sxs-lookup"><span data-stu-id="5e1b2-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5e1b2-125"><strong>FestlegenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="5e1b2-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="5e1b2-126"><strong>Name</strong>: Meinevar<strong>Ausdruck</strong>: InputBox (&quot;Geben Sie eine Zahl ungleich NULL.&quot;)</span><span class="sxs-lookup"><span data-stu-id="5e1b2-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e1b2-127">[TempVars]! [Meinevar] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="5e1b2-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="5e1b2-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="5e1b2-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5e1b2-129"><strong>Meldung</strong>: =&quot;eingegebene &quot; &amp; [TempVars]! [Meinevar] &amp; &quot;. &quot; <strong>Signalton</strong>: <strong>YesType</strong>: <strong>Informationen</strong></span><span class="sxs-lookup"><span data-stu-id="5e1b2-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5e1b2-130"><strong>EntfernenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="5e1b2-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="5e1b2-131"><strong>Name</strong>: MeineVar</span><span class="sxs-lookup"><span data-stu-id="5e1b2-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

