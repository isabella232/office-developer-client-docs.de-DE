---
title: Recordset2.Update-Methode (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 996686501d355555814a48bc665f3eb634a74298
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998616"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="057a9-102">Recordset2.Update-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="057a9-102">Recordset2.Update method (DAO)</span></span>

<span data-ttu-id="057a9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="057a9-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="057a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="057a9-104">Syntax</span></span>

<span data-ttu-id="057a9-105">*Ausdruck* . Update (***UpdateType***, ***erzwingen***)</span><span class="sxs-lookup"><span data-stu-id="057a9-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="057a9-106">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="057a9-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="057a9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="057a9-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="057a9-108">Name</span><span class="sxs-lookup"><span data-stu-id="057a9-108">Name</span></span></p></th>
<th><p><span data-ttu-id="057a9-109">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="057a9-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="057a9-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="057a9-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="057a9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="057a9-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="057a9-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="057a9-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="057a9-113">Optional</span><span class="sxs-lookup"><span data-stu-id="057a9-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="057a9-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="057a9-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="057a9-115">Eine <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> -Konstante, die den Aktualisierungstyp so angibt, wie er in den Einstellungen angegeben ist (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="057a9-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="057a9-116"><em>Force</em></span><span class="sxs-lookup"><span data-stu-id="057a9-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="057a9-117">Optional</span><span class="sxs-lookup"><span data-stu-id="057a9-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="057a9-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="057a9-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="057a9-p101">Ein <strong>Boolean</strong> -Wert, der angibt, ob die Änderungen in der Datenbank unabhängig davon erzwungen werden sollen, ob die zugrunde liegenden Daten von einem anderen Benutzer seit dem <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong> -, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> - oder <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> -Aufruf geändert wurden. Falls <strong>True</strong>, werden die Änderungen erzwungen und Änderungen anderer Benutzer werden einfach überschrieben. Falls <strong>False</strong> (Standard), verursachen Änderungen eines anderen Benutzers, während die Aktualisierung noch aussteht, das Fehlschlagen der Aktualisierung für die Änderungen, die einen Konflikt verursachen. Es treten keine Fehler auf, aber die <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> - und <strong>BatchCollisions</strong> -Eigenschaften geben die Anzahl der Konflikte bzw. die Anzahl der Zeilen an, die von Konflikten betroffen sind (nur ODBCDirect-Arbeitsbereiche).  </span><span class="sxs-lookup"><span data-stu-id="057a9-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="057a9-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="057a9-123">Remarks</span></span>

<span data-ttu-id="057a9-124">Verwenden Sie **Update**, um den aktuellen Datensatz und alle daran vorgenommenen Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="057a9-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="057a9-125">[!WICHTIG] Änderungen an dem aktuellen Datensatz gehen in folgenden Fällen verloren:</span><span class="sxs-lookup"><span data-stu-id="057a9-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="057a9-126">Sie verwenden die **Edit**- oder **AddNew**-Methode und wechseln dann zu einem anderen Datensatz, ohne zuvor **Update** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="057a9-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="057a9-127">Sie verwenden **Edit** oder **AddNew** und dann erneut **Edit** oder **AddNew**, ohne zuvor **Update** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="057a9-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="057a9-128">Sie legen die **[Bookmark](recordset2-bookmark-property-dao.md)** -Eigenschaft auf einen anderen Datensatz fest.</span><span class="sxs-lookup"><span data-stu-id="057a9-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="057a9-129">Sie schließen das **Recordset**, ohne zuvor **Update** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="057a9-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="057a9-130">Sie brechen den **Edit**-Vorgang ab, indem Sie **[CancelUpdate](recordset2-cancelupdate-method-dao.md)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="057a9-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="057a9-p102">Wenn Sie einen Datensatz bearbeiten möchten, verwenden Sie die **Edit**-Methode, um den Inhalt des aktuellen Datensatzes in den Kopierpuffer zu kopieren. Ohne vorheriges Anwenden von **Edit** tritt ein Fehler auf, sobald Sie **Update** verwenden oder versuchen, den Wert eines Felds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="057a9-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="057a9-133">In einem ODBCDirect-Arbeitsbereich können Sie Batchaktualisierungen vornehmen, wenn die Cursor-Bibliothek dies unterstützt und das **Recordset** mit der Option der optimistischen Batchsperre geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="057a9-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="057a9-134">Ist in einem Microsoft Access-Arbeitsbereich die **LockEdits**-Eigenschafteneinstellung eines **Recordset**-Objekts in einer Mehrbenutzerumgebung auf **True** festgelegt (pessimistisch gesperrt), bleibt der Datensatz ab dem Moment gesperrt, in dem **Edit** verwendet wird, bis zu dem Zeitpunkt, zu dem die **Update**-Methode ausgeführt oder die Bearbeitung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="057a9-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="057a9-135">Wenn die **LockEdits**-Eigenschafteneinstellung auf **False** festgelegt ist (optimistisch gesperrt), wird der Datensatz gesperrt und mit dem vorab bearbeiteten Datensatz verglichen, bevor er in der Datenbank aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="057a9-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="057a9-136">Wurde der Datensatz nach dem Verwenden der **Edit**-Methode geändert, schlägt der **Update**-Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="057a9-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="057a9-137">Die mit einem Microsoft Access-Datenbankmodul verbundenen ODBC- und installierbaren ISAM-Datenbanken verwenden immer optimistische Sperren.</span><span class="sxs-lookup"><span data-stu-id="057a9-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="057a9-138">Verwenden Sie erneut die **Update**-Methode, um den **Update**-Vorgang mit Ihren Änderungen fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="057a9-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="057a9-139">Zum Zurücksetzen auf als anderer Benutzer den Datensatz geändert, aktualisieren Sie den aktuellen Datensatz mit Move 0.</span><span class="sxs-lookup"><span data-stu-id="057a9-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="057a9-p104">[!HINWEIS] Es muss ein eindeutiger Index für den Datensatz in der zugrunde liegenden Datenquelle vorhanden sein, damit ein Datensatz hinzugefügt, bearbeitet oder gelöscht werden kann. Andernfalls tritt im Methodenaufruf **AddNew**, **Delete** oder **Edit** in einem Microsoft Access-Arbeitsbereich ein Fehler vom Typ "Berechtigung verweigert" auf, oder im **Update**-Aufruf in einem ODBCDirect-Arbeitsbereich tritt ein Fehler vom Typ "Ungültiges Argument" auf.</span><span class="sxs-lookup"><span data-stu-id="057a9-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


