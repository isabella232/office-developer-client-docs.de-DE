---
title: AbbrechenEreignis-Makroaktion
TOCTitle: CancelEvent Macro Action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0bc9f38e1f91a58fcfc7cedfdfb740a22477f649
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880670"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="90e4e-102">AbbrechenEreignis-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="90e4e-102">CancelEvent Macro Action</span></span>


<span data-ttu-id="90e4e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90e4e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="90e4e-104">Die **AbbrechenEreignis** -Aktion können Sie das Ereignis abzubrechen, das Zugriff auf das Makro mit dieser Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e4e-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="90e4e-105">Der Name des Makros ist die Einstellung einer Ereigniseigenschaft wie **BeforeUpdate**, **OnOpen**, **OnUnload**oder **OnPrint**.</span><span class="sxs-lookup"><span data-stu-id="90e4e-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="90e4e-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="90e4e-106">Setting</span></span>

<span data-ttu-id="90e4e-107">Die **AbbrechenEreignis** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="90e4e-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="90e4e-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="90e4e-108">Remarks</span></span>

<span data-ttu-id="90e4e-p102">In einem Formular verwenden Sie die **AbbrechenEreignis** -Aktion üblicherweise in einem Gültigkeitsprüfungsmakro mit der **VorAktualisierung** -Ereigniseigenschaft. Wenn ein Benutzer Daten in ein Steuerelement oder in einen Datensatz eingibt, führt Access zunächst das Makro aus und fügt dann der Datenbank die Daten hinzu. Wenn die Daten die Bedingungen der Gültigkeitsprüfung im Makro nicht erfüllen, bricht die **AbbrechenEreignis** -Aktion den Aktualisierungsvorgang vor dem Starten ab.</span><span class="sxs-lookup"><span data-stu-id="90e4e-p102">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property. When a user enters data in a control or record, Access runs the macro before adding the data to the database. If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="90e4e-112">Diese Aktion wird häufig zusammen mit der **Meldungsfeld** -Aktion verwendet, um anzugeben, dass die Daten die Bedingungen der Gültigkeitsprüfung nicht erfüllen, und um nützliche Informationen zu der Art von Daten bereitzustellen, die eingegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="90e4e-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="90e4e-113">Die folgenden Ereignisse können von der **AbbrechenEreignis** -Aktion abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="90e4e-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e4e-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e4e-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-124"><strong>Format</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="90e4e-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e4e-129"><strong>Delete</strong></span><span class="sxs-lookup"><span data-stu-id="90e4e-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="90e4e-130">[!HINWEIS] Sie können die **AbbrechenEreignis** -Aktion mit dem **MouseDown** -Ereignis nur dazu verwenden, das Ereignis abzubrechen, das beim Klicken mit der rechten Maustaste auftritt.</span><span class="sxs-lookup"><span data-stu-id="90e4e-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="90e4e-131">Wenn die **BeimDoppelklicken** -Ereigniseigenschaft ein Makro angibt, das die **AbbrechenEreignis** -Aktion enthält, wird durch diese Aktion das **DblClick** -Ereignis abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="90e4e-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="90e4e-p103">Nachdem das Makro für das Ereignis ausgeführt wurde, tritt für Ereignisse, die abgebrochen werden können, das Standardverhalten für das Ereignis ein (d. h. das Verhalten, das Access normalerweise zeigt, wenn das Ereignis eintritt). Auf diese Weise können Sie das Standardverhalten abbrechen. Wenn Sie beispielsweise auf ein Wort doppelklicken, auf dem sich die Einfügemarke in einem Textfeld befindet, wird das Wort normalerweise in Access markiert. Sie können dieses Standardverhalten in dem Makro für das **DblClick** -Ereignis abbrechen und eine andere Aktion ausführen, z. B. das Öffnen eines Formulars, das Information zu den Daten in dem Textfeld enthält. Für Ereignisse, die nicht abgebrochen werden können, tritt das Standardverhalten ein, bevor das Makro ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90e4e-p103">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs. This enables you to cancel the default behavior. For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word. You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box. For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="90e4e-p104">[!HINWEIS] Wenn die **BeiEntladen** -Ereigniseigenschaft eines Formulars ein Makro angibt, das eine **AbbrechenEreignis** -Aktion ausführt, können Sie das Formular nicht schließen. Sie müssen entweder die Bedingung berichtigen, die das Ausführen der **AbbrechenEreignis** -Aktion verursacht hat, oder das Makro öffnen und die **AbbrechenEreignis** -Aktion löschen. Wenn es sich bei dem Formular um ein modales Formular handelt, können Sie das Makro nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="90e4e-p104">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form. You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action. If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="90e4e-140">Verwenden Sie die **CancelEvent** -Methode des **DoCmd** -Objekts, um die **AbbrechenEreignis** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="90e4e-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="90e4e-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="90e4e-141">Example</span></span>

<span data-ttu-id="90e4e-142"> Überprüfen der Gültigkeit von Daten mithilfe eines Makros</span><span class="sxs-lookup"><span data-stu-id="90e4e-142">Validate data by using a macro</span></span>

<span data-ttu-id="90e4e-p105">Mit dem folgenden Gültigkeitsprüfungsmakro werden die Postleitzahlen überprüft, die im Formular Lieferanten eingegeben werden. Es zeigt die Verwendung der Aktionen StoppMakro, Meldungsfeld, AbbrechenEreignis und GeheZuSteuerelement. Mit einem Bedingungsausdruck werden das Land, die Region und die Postleitzahl überprüft, die im Formular in einem Datensatz eingegeben werden. Wenn die Postleitzahl nicht das richtige Format für das Land oder die Region aufweist, wird vom Makro ein Meldungsfeld angezeigt, und das Speichern des Datensatzes wird abgebrochen. Sie kehren dann zum Steuerelement Postleitzahl zurück, in dem Sie den Fehler korrigieren können. Dieses Makro sollte mit der BeforeUpdate-Eigenschaft des Formulars Lieferanten verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="90e4e-p105">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the Postal Code control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90e4e-149">Bedingung</span><span class="sxs-lookup"><span data-stu-id="90e4e-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="90e4e-150">Aktion</span><span class="sxs-lookup"><span data-stu-id="90e4e-150">Action</span></span></p></th>
<th><p><span data-ttu-id="90e4e-151">Argumente: Einstellung</span><span class="sxs-lookup"><span data-stu-id="90e4e-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="90e4e-152">Kommentar</span><span class="sxs-lookup"><span data-stu-id="90e4e-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="90e4e-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="90e4e-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="90e4e-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="90e4e-155">Wenn Land/Region den Wert Null hat, kann die Postleitzahl nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="90e4e-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e4e-156">[Land/Region] In (&quot;Frankreich&quot;,&quot;Italien&quot;,&quot;Spanien&quot;) und Len ([Postleitzahl]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="90e4e-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="90e4e-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="90e4e-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="90e4e-158">Meldung: Die Postleitzahl muss 5 Zeichen lang sein. 

</span><span class="sxs-lookup"><span data-stu-id="90e4e-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="90e4e-159">Signalton: <strong>Ja</strong> Typ: <strong>Informationen</strong> Titel: Postleitzahl fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="90e4e-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="90e4e-160">Zeigt eine Meldung an, wenn die Postleitzahl nicht 5 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="90e4e-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-161">...</span><span class="sxs-lookup"><span data-stu-id="90e4e-161"></span></span></p></td>
<td><p><span data-ttu-id="90e4e-162">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="90e4e-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="90e4e-163">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="90e4e-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="90e4e-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="90e4e-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="90e4e-165">Steuerelementname: Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="90e4e-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-166">[Land/Region] In (&quot;Australien&quot;,&quot;Singapur&quot;) und Len ([Postleitzahl]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="90e4e-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="90e4e-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="90e4e-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="90e4e-168">Meldung: Die Postleitzahl muss 4 Zeichen lang sein. 

</span><span class="sxs-lookup"><span data-stu-id="90e4e-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="90e4e-169">Signalton: <strong>Ja</strong> Typ: <strong>Informationen</strong> Titel: Postleitzahl fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="90e4e-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="90e4e-170">Zeigt eine Meldung an, wenn die Postleitzahl nicht 4 Zeichen lang ist.</span><span class="sxs-lookup"><span data-stu-id="90e4e-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e4e-171">...</span><span class="sxs-lookup"><span data-stu-id="90e4e-171"></span></span></p></td>
<td><p><span data-ttu-id="90e4e-172">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="90e4e-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="90e4e-173">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="90e4e-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="90e4e-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="90e4e-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="90e4e-175">Steuerelementname: Postleitzahl</span><span class="sxs-lookup"><span data-stu-id="90e4e-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e4e-176">([Land/Region] = &quot;Kanada&quot;) Und ([Postleitzahl] nicht wie&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="90e4e-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="90e4e-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="90e4e-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="90e4e-178">Meldung: Die Postleitzahl ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="90e4e-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="90e4e-179">Beispiel für Kanadische Code: H1J 1 c 3 Signalton: <strong>Ja</strong> Typ: <strong>Informationen</strong> Titel: Postleitzahl Codefehler</span><span class="sxs-lookup"><span data-stu-id="90e4e-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="90e4e-p109">Zeigt eine Meldung an, wenn eine für Kanada ungültige Postleitzahl angegeben wird. (Beispiel für eine kanadische Postleitzahl: H1J 1C3).</span><span class="sxs-lookup"><span data-stu-id="90e4e-p109">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e4e-182">...</span><span class="sxs-lookup"><span data-stu-id="90e4e-182"></span></span></p></td>
<td><p><span data-ttu-id="90e4e-183">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="90e4e-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="90e4e-184">Bricht das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="90e4e-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

