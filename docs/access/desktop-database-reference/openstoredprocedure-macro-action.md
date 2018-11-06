---
title: OpenStoredProcedure-Makroaktion
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dba3d57a1b9ce890898ac2f5b76b916b848c5a9b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997518"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="15378-102">OpenStoredProcedure-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="15378-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="15378-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15378-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15378-p101">In einem Access-Projekt können Sie die **ÖffnenGespeicherteProzedur**-Aktion zum Öffnen einer gespeicherten Prozedur in der Datenblattansicht, der Entwurfsansicht der gespeicherten Prozedur oder der Seitenansicht verwenden. Diese Aktion führt die gespeicherte benannte Prozedur aus, wenn sie in der Datenblattansicht geöffnet wird. Sie können den Dateneingabemodus für die gespeicherte Prozedur auswählen und die Datensätze einschränken, die von der gespeicherten Prozedur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15378-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="15378-107">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="15378-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="15378-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="15378-108">Setting</span></span>

<span data-ttu-id="15378-109">Die **ÖffnenGespeicherteProzedur**-Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="15378-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15378-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="15378-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="15378-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15378-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15378-112"><strong>Prozedurname</strong></span><span class="sxs-lookup"><span data-stu-id="15378-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="15378-113">Der Name der gespeicherten Prozedur zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="15378-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="15378-114">Das <strong>Prozedurname</strong> Feld im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle gespeicherten Prozeduren in der aktuellen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="15378-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="15378-115">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="15378-115">This is a required argument.</span></span> <span data-ttu-id="15378-116">Wenn Sie ein Makro ausführen, das die <strong>ÖffnenGespeicherteProzedur</strong>-Aktion in einer Bibliotheksdatenbank verwendet, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach der gespeicherten Prozedur mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="15378-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15378-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="15378-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="15378-p103">Die Ansicht, in der die gespeicherte Prozedur geöffnet wird. Klicken Sie im Feld <strong>Ansicht</strong> auf <strong>Datenblatt</strong>, <strong>Entwurf</strong>, <strong>Seitenansicht</strong>, <strong>PivotTable</strong> oder <strong>PivotChart</strong>. Die Standardeinstellung ist <strong>Datenblatt</strong>.</span><span class="sxs-lookup"><span data-stu-id="15378-p103">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15378-121"><strong>Data Mode</strong></span><span class="sxs-lookup"><span data-stu-id="15378-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="15378-p104">Der Dateneingabemodus für die gespeicherte Prozedur. Dieser gilt nur für gespeicherte Prozeduren, die in der Datenblattansicht geöffnet werden. Klicken Sie auf <strong>Hinzufügen</strong> (der Benutzer kann neue Datensätze hinzufügen, jedoch vorhandene Datensätze nicht anzeigen oder bearbeiten), <strong>Bearbeiten</strong> (der Benutzer kann vorhandene Datensätze anzeigen oder bearbeiten und neue Datensätze hinzufügen) oder <strong>Nur lesen</strong> (der Benutzer kann die Datensätze nur anzeigen). Die Standardeinstellung ist <strong>Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="15378-p104">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="15378-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15378-126">Remarks</span></span>

<span data-ttu-id="15378-127">Diese Aktion ist mit dem Doppelklicken auf die gespeicherte Prozedur im Navigationsbereich, dem Klicken auf die gespeicherte Prozedur im Navigationsbereich mit der rechten Maustaste und dem Auswählen des gewünschten Befehls vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="15378-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="15378-p105">Durch das Wechseln zur Entwurfsansicht, während die gespeicherte Prozedur geöffnet ist, wird die Einstellung des Arguments **Datenmodus** für die gespeicherte Prozedur entfernt. Diese Einstellung ist nicht aktiv, selbst wenn der Benutzer zur Datenblattansicht zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="15378-p105">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="15378-130">Sie können eine gespeicherte Prozedur im Navigationsbereich an eine Makro-Aktionszeile ziehen.</span><span class="sxs-lookup"><span data-stu-id="15378-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="15378-131">Dadurch wird automatisch eine **ÖffnenGespeicherteProzedur** -Aktion, die die gespeicherte Prozedur in der Datenblattansicht geöffnet wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="15378-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="15378-132">
						Wenn Sie die Systemmeldungen nicht anzeigen möchten, die normalerweise angezeigt werden, wenn eine gespeicherten Prozedur ausgeführt wird (sie melden, dass es sich um eine gespeicherte Prozedur handelt und auf wie viele Datensätze sie sich auswirkt), können Sie die \*\*Warnmeldungen\*\*-Aktion verwenden, um die Anzeige dieser Meldungen zu unterdrücken.
</span><span class="sxs-lookup"><span data-stu-id="15378-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="15378-133">Verwenden Sie die **OpenStoredProcedure**-Methode des **DoCmd**-Objekts, um die **ÖffnenGespeicherteProzedur**-Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="15378-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

