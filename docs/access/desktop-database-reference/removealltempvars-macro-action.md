---
title: EntfernenAlleTempVar-Makroaktion
TOCTitle: RemoveAllTempVars Macro Action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 42217fea05b29fdf127945d1547adbac28346cc9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474139"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="f92f8-102">EntfernenAlleTempVar-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="f92f8-102">RemoveAllTempVars Macro Action</span></span>


<span data-ttu-id="f92f8-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f92f8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="f92f8-104">Mit der **EntfernenAlleTempVar** -Aktion können Sie alle mit der **FestlegenTempVar** -Aktion erstellten temporären Variablen entfernen.</span><span class="sxs-lookup"><span data-stu-id="f92f8-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="f92f8-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f92f8-105">Setting</span></span>

<span data-ttu-id="f92f8-106">Die **EntfernenAlleTempVar** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="f92f8-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="f92f8-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f92f8-107">Remarks</span></span>

  - <span data-ttu-id="f92f8-p101">Es können bis zu 255 temporäre Variablen gleichzeitig definiert sein. Wenn eine temporäre Variable nicht entfernt wird, verbleibt diese bis zum Schließen der Datenbank oder des Projekts im Arbeitsspeicher. Es empfiehlt sich, temporäre Variablen zu entfernen, sobald Sie deren Verwendung beendet haben.</span><span class="sxs-lookup"><span data-stu-id="f92f8-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database or project. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="f92f8-111">Beim Schließen der Datenbank oder des Projekts werden von Access automatisch alle temporären Variablen entfernt.</span><span class="sxs-lookup"><span data-stu-id="f92f8-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="f92f8-112">Verwenden Sie zum Entfernen einer einzelnen temporären Variable die **EntfernenTempVar** -Aktion, und legen Sie die Argumente auf den Namen der zu entfernenden temporären Variable fest.</span><span class="sxs-lookup"><span data-stu-id="f92f8-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="f92f8-113">Verwenden Sie zum Ausführen der **EntfernenAlleTempVar** -Aktion in einem VBA-Modul die **RemoveAll** -Methode des **TempVars** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f92f8-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="f92f8-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f92f8-114">Example</span></span>

<span data-ttu-id="f92f8-115">Im folgenden Makro wird die Vorgehensweise zum Erstellen einer temporären Variable, zum Verwenden der Variable in einer Bedingung und einem Meldungsfeld und zum folgenden Entfernen der Variable mit der **EntfernenAlleTempVar** -Aktion gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f92f8-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f92f8-116">Bedingung</span><span class="sxs-lookup"><span data-stu-id="f92f8-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="f92f8-117">Aktion</span><span class="sxs-lookup"><span data-stu-id="f92f8-117">Action</span></span></p></th>
<th><p><span data-ttu-id="f92f8-118">Argumente</span><span class="sxs-lookup"><span data-stu-id="f92f8-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f92f8-119"><strong>FestlegenTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="f92f8-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="f92f8-120"><strong>Name</strong>: Meinevar<strong>Ausdruck</strong>: InputBox (&quot;Geben Sie eine Zahl ungleich NULL.&quot;)</span><span class="sxs-lookup"><span data-stu-id="f92f8-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f92f8-121">[TempVars]! [Meinevar] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="f92f8-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="f92f8-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="f92f8-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="f92f8-123"><strong>Meldung</strong>: =&quot;eingegebene &quot; &amp; [TempVars]! [Meinevar] &amp; &quot;. &quot; <strong>Signalton</strong>: <strong>YesType</strong>: <strong>Informationen</strong></span><span class="sxs-lookup"><span data-stu-id="f92f8-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="f92f8-124"><strong>EntfernenAlleTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="f92f8-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

