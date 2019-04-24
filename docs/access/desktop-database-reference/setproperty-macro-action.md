---
title: SetProperty-Makroaktion
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314574"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="f165c-102">SetProperty-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="f165c-102">SetProperty macro action</span></span>

<span data-ttu-id="f165c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f165c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f165c-104">Sie können die **FestlegenEigenschaft** -Aktion verwenden, um eine Eigenschaft für ein Steuerelement in einem Formular oder Bericht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f165c-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="f165c-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="f165c-105">Setting</span></span>

<span data-ttu-id="f165c-106">Die **FestlegenEigenschaft**-Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="f165c-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f165c-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="f165c-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f165c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f165c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f165c-109">Steuerelementname</span><span class="sxs-lookup"><span data-stu-id="f165c-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="f165c-110">Geben Sie den Namen des Felds oder Steuerelements ein, für das Sie den Eigenschaftswert festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="f165c-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="f165c-111">Verwenden Sie lediglich den Namen des Steuerelements, nicht die vollständige Syntax.</span><span class="sxs-lookup"><span data-stu-id="f165c-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="f165c-112">Lassen Sie das Argument leer, um die Eigenschaft für das aktuelle Formular oder den aktuellen Bericht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f165c-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f165c-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f165c-113">Property</span></span></p></td>
<td><p><span data-ttu-id="f165c-p102">Wählen Sie die Eigenschaft aus, die Sie festlegen möchten. Der Abschnitt <strong>Hinweise</strong> in diesem Artikel enthält eine Auflistung der Eigenschaften, die mithilfe dieser Aktion festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="f165c-p102">Select the property that you want to set. See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f165c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f165c-116">Value</span></span></p></td>
<td><p><span data-ttu-id="f165c-117">Geben Sie den Wert ein, auf den die Eigenschaft festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f165c-117">Type the value that the property is to be set to.</span></span> <span data-ttu-id="f165c-118">Für Eigenschaften, deren Werte entweder "Ja" oder "Nein" sind, verwenden Sie <strong>-1</strong> für Yes und <strong>0</strong> für Nein.</span><span class="sxs-lookup"><span data-stu-id="f165c-118">For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f165c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f165c-119">Remarks</span></span>

- <span data-ttu-id="f165c-120">Mithilfe der **FestlegenEigenschaft**-Aktion können Sie die folgenden Eigenschaften eines Steuerelements festlegen: **Aktiviert**, **Sichtbar**, **Gesperrt**, **Links**, **Oben**, **Breite**, **Höhe**, **Textfarbe**, **Hintergrundfarbe** oder **Beschriftung**.</span><span class="sxs-lookup"><span data-stu-id="f165c-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="f165c-121">Wenn Sie einen ungültigen Wert für das Argument ***Wert*** eingeben, tritt kein Fehler auf. Allerdings kann es passieren, dass Access die Eigenschaft in einen anderen Wert ändert. Dies hängt davon ab, wie das Argument interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="f165c-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="f165c-p104">Sie können die **FestlegenEigenschaft** -Aktion nur dann in einem eigenständigen Makro verwenden, wenn eine Aktion vorangeht, mit der das Formular oder der Bericht ausgewählt wird, in dem das Steuerelement enthalten ist, für das Sie die Eigenschaft festlegen. Wenn das Formular oder der Bericht noch nicht geöffnet ist, verwenden Sie zum Öffnen und Auswählen die Aktion **ÖffnenFormular** bzw. **ÖffnenBericht**. Ist das Formular oder der Bericht geöffnet, können Sie es bzw. ihn mit der **AuswählenObjekt** -Aktion auswählen. Legen Sie die Eigenschaft dann mithilfe der **FestlegenEigenschaft** -Aktion fest. Sie müssen das Objekt nicht auswählen, wenn Sie die **FestlegenEigenschaft** -Aktion in einem Makro verwenden, das in ein Steuerelement eingebettet ist, das sich auf demselben Formular oder in demselben Bericht befindet wie das Steuerelement, für das Sie die Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="f165c-p104">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="f165c-127">Verwenden Sie die **FestlegenEigenschaft** -Methode des **DoCmd** -Objekts, um die **FestlegenEigenschaft** -Aktion in einem VBA-Modul auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f165c-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="f165c-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f165c-128">Example</span></span>

<span data-ttu-id="f165c-129">Das folgende Beispiel zeigt, wie Sie mit der SetProperty-Aktion die Sichtbarkeit des \*\*\*\* Textfelds myTextBox umschalten.</span><span class="sxs-lookup"><span data-stu-id="f165c-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="f165c-130">**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f165c-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
