---
title: Recordset.RecordsetType-Eigenschaft (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e4babfce754ec0e9c4744142570054c0249936f8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026211"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="1e887-102">Recordset.RecordsetType-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e887-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="1e887-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e887-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e887-p101">Sie können mit der **RecordsetType** -Eigenschaft angeben, welche Art von Recordset für ein Formular bereit gestellt wird. **Byte** -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1e887-p101">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form. Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e887-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e887-106">Syntax</span></span>

<span data-ttu-id="1e887-107">*Ausdruck* . RecordsetType</span><span class="sxs-lookup"><span data-stu-id="1e887-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="1e887-108">*expression*  Eine Variable, die ein **Form**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e887-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e887-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e887-109">Remarks</span></span>

<span data-ttu-id="1e887-110">Die **RecordsetType** -Eigenschaft verwendet die folgenden Einstellungen in einer Microsoft Access-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1e887-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e887-111">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1e887-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="1e887-112">Recordset-Typ</span><span class="sxs-lookup"><span data-stu-id="1e887-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="1e887-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e887-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e887-114">0</span><span class="sxs-lookup"><span data-stu-id="1e887-114">0</span></span></p></td>
<td><p><span data-ttu-id="1e887-115">Dynaset</span><span class="sxs-lookup"><span data-stu-id="1e887-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="1e887-116">(Standardeinstellung) Sie können gebundene Steuerelemente auf der Basis einer einzigen Tabelle oder von Tabellen mit einer 1:1-Beziehung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1e887-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="1e887-117">Für auf Grundlage von Tabellen mit einer 1: n-Beziehung Felder gebundenen Steuerelemente, können nicht Sie Daten aus dem Feld Join bearbeiten, klicken Sie auf die &quot;eine&quot; Seite der Beziehung, es sei denn, Aktualisierungsweitergabe zwischen den Tabellen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1e887-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e887-118">1</span><span class="sxs-lookup"><span data-stu-id="1e887-118">1</span></span></p></td>
<td><p><span data-ttu-id="1e887-119">Dynaset (Unregelmäßige Aktualisierungen)</span><span class="sxs-lookup"><span data-stu-id="1e887-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="1e887-120">Alle Tabellen und an ihre Felder gebundenen Steuerelemente können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1e887-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e887-121">2</span><span class="sxs-lookup"><span data-stu-id="1e887-121">2</span></span></p></td>
<td><p><span data-ttu-id="1e887-122">Snapshot</span><span class="sxs-lookup"><span data-stu-id="1e887-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="1e887-123">Es können keine Tabellen oder an ihre Felder gebundenen Steuerelemente bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1e887-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1e887-124">[!HINWEIS] Wenn Sie vermeiden möchten, dass Daten in gebundenen Steuerelementen bearbeitet werden, wenn das Formular in der Formularansicht oder Datenblattansicht angezeigt wird, können Sie die **RecordsetType** -Eigenschaft auf 2 festlegen.</span><span class="sxs-lookup"><span data-stu-id="1e887-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="1e887-125">Die **RecordsetType** -Eigenschaft verwendet die folgenden Einstellungen in einem Microsoft Access-Projekt (ADP).</span><span class="sxs-lookup"><span data-stu-id="1e887-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e887-126">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1e887-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="1e887-127">Recordset-Typ</span><span class="sxs-lookup"><span data-stu-id="1e887-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="1e887-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e887-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e887-129">3</span><span class="sxs-lookup"><span data-stu-id="1e887-129">3</span></span></p></td>
<td><p><span data-ttu-id="1e887-130">Snapshot</span><span class="sxs-lookup"><span data-stu-id="1e887-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="1e887-131">Es können keine Tabellen oder an ihre Felder gebundenen Steuerelemente bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1e887-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e887-132">4</span><span class="sxs-lookup"><span data-stu-id="1e887-132">4</span></span></p></td>
<td><p><span data-ttu-id="1e887-133">Aktualisierbarer Snapshot</span><span class="sxs-lookup"><span data-stu-id="1e887-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="1e887-134">(Standardeinstellung) Alle Tabellen und an ihre Felder gebundenen Steuerelemente können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1e887-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1e887-135">[!HINWEIS] Wenn die **RecordsetType** -Eigenschaft eines geöffneten Formulars oder Berichts geändert wird, führt dies zu einer automatischen Neuerstellung der Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="1e887-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="1e887-p103">Sie können Formulare erstellen, die auf mehreren zugrunde liegenden Tabellen basieren, an deren Felder Steuerelemente in den Formularen gebunden sind. Abhängig von der Einstellung der **RecordsetType** -Eigenschaft können Sie einschränken, welche gebundenen Steuerelemente bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="1e887-p103">You can create forms based on multiple underlying tables with fields bound to controls on the forms. Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="1e887-p104">Zusätzlich zu dem von der **RecordsetType** -Eigenschaft bereitgestellten Bearbeitungssteuerelement verfügt jedes Steuerelement in einem Formular über eine **Locked** -Eigenschaft, mit der Sie angeben können, ob das Steuerelement und die ihm zugrunde liegenden Daten bearbeitet werden können. Ist die **Locked** -Eigenschaft auf Ja festgelegt, können die Daten nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1e887-p104">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited. If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="1e887-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1e887-140">Example</span></span>

<span data-ttu-id="1e887-p105">Im folgenden Beispiel können Datensätze nur dann aktualisiert werden, wenn die Benutzer-ID ADMIN lautet. In diesem Codebeispiel wird die **RecordsetType**-Eigenschaft auf Snapshot festgelegt, wenn die öffentliche Variable gstrUserID nicht den Wert ADMIN hat.</span><span class="sxs-lookup"><span data-stu-id="1e887-p105">In the following example, only if the user ID is ADMIN can records be updated. This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="1e887-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e887-143">See also</span></span>

- [<span data-ttu-id="1e887-144">Form-Objekt</span><span class="sxs-lookup"><span data-stu-id="1e887-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


