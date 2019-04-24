---
title: Connection. Execute-Methode (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295912"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="43d55-102">Connection. Execute-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="43d55-102">Connection.Execute method (DAO)</span></span>

<span data-ttu-id="43d55-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43d55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43d55-104">Führt eine Aktionsabfrage oder eine SQL-Anweisung zu dem angegebenen Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="43d55-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43d55-105">Syntax</span></span>

<span data-ttu-id="43d55-106">*Ausdruck* . Execute (***Abfrage***, ***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="43d55-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="43d55-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="43d55-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="43d55-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="43d55-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43d55-109">Name</span><span class="sxs-lookup"><span data-stu-id="43d55-109">Name</span></span></p></th>
<th><p><span data-ttu-id="43d55-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="43d55-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="43d55-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="43d55-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="43d55-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43d55-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43d55-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="43d55-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="43d55-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="43d55-114">Required</span></span></p></td>
<td><p><span data-ttu-id="43d55-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-116">Ein <strong>String</strong>-Wert, der eine SQL-Anweisung oder den <strong>Name</strong>-Eigenschaftswert eines <strong>QueryDef</strong>-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="43d55-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d55-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="43d55-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="43d55-118">Optional</span><span class="sxs-lookup"><span data-stu-id="43d55-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="43d55-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-120">Eine Konstante oder eine Kombination aus Konstanten, durch die die Datenintegritätsmerkmale der Abfrage festgelegt sind, wie unter Einstellungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43d55-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="43d55-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43d55-121">Remarks</span></span>

<span data-ttu-id="43d55-122">Sie können die folgenden **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** -Konstanten für Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="43d55-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43d55-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="43d55-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="43d55-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43d55-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43d55-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-126">Verweigert anderen Benutzern die Schreibberechtigung (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="43d55-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d55-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-128">(Standardeinstellung) Führt inkonsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="43d55-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43d55-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-130">Führt konsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="43d55-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d55-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-p101">Führt eine SQL-Pass-Through-Abfrage aus. Wenn Sie diese Option festlegen, wird die SQL-Anweisung zur Verarbeitung an eine ODBC-Datenbank übergeben (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="43d55-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43d55-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-135">Führt ein Rollback für Updates aus, wenn ein Fehler auftritt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="43d55-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d55-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-137">Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="43d55-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43d55-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-139">Führt die Abfrage asynchron aus (nur ODBCDirect-Connection- und -QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="43d55-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43d55-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="43d55-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="43d55-141">Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="43d55-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="43d55-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="43d55-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="43d55-p103">[!HINWEIS] Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können eins von beiden, jedoch nicht beide in einer angegebenen Instanz von **OpenRecordset** verwenden. Durch die Verwendung der **dbConsistent** - und **dbInconsistent** -Konstanten wird ein Fehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="43d55-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="43d55-p104">Die **Execute** -Methode ist nur für Aktionsabfragen gültig. Wenn Sie die **Execute** -Methode mit einem anderen Abfragetyp verwenden, tritt ein Fehler auf. Da eine Aktionsabfrage keine Datensätze zurückgibt, gibt die **Execute** -Methode keinen **Datensatz** zurück. (Durch Ausführen einer SQL-Pass-Through-Abfrage in einem ODBCDirect-Arbeitsbereich wird kein Fehler zurückgegeben, wenn kein **Datensatz** zurückgegeben wird).</span><span class="sxs-lookup"><span data-stu-id="43d55-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="43d55-p105">Verwenden Sie die **RecordsAffected** -Eigenschaft des **Connection** -, **Database** - oder **QueryDef** -Objekts, um die Anzahl der von der aktuellsten **Execute** -Methode betroffenen Datensätze zu ermitteln. **RecordsAffected** enthält beispielsweise die Anzahl gelöschter, aktualisierter oder eingefügter Datensätze bei der Ausführung einer Aktionsabfrage. Wenn Sie zum Ausführen einer Abfrage die **Execute** -Methode verwenden, wird bei der **RecordsAffected** -Eigenschaft des **QueryDef** -Objekts die Anzahl der betroffenen Datensätze festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43d55-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="43d55-p106">In einem Microsoft Access-Arbeitsbereich erzeugt die **Execute** -Methode keinen Fehler, wenn Sie eine syntaktisch korrekte SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen - sogar dann, wenn keine einzige Zeile bearbeitet oder gelöscht werden kann. Verwenden Sie deshalb immer die **dbFailOnError** -Option, wenn Sie zum Ausführen eines Updates oder zum Löschen einer Abfrage die **Execute** -Methode. Diese Option generiert einen Laufzeitfehler und setzt alle erfolgreichen Änderungen zurück, wenn einer der betroffenen Datensätze gesperrt ist und deshalb nicht aktualisiert oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="43d55-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="43d55-p107">In früheren Versionen des Microsoft Jet-Datenbankmoduls werden SQL-Anweisungen automatisch in implizite Transaktionen integriert. Wenn ein Teil einer Anweisung, die mit **dbFailOnError** ausgeführt wurde, einen Fehler verursacht, würde die gesamte Anweisung zurückgesetzt. Um die Leistung zu verbessern, wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie einen älteren DAO-Code aktualisieren, sollten Sie erwägen, explizite Transaktionen um **Execute** -Anweisungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="43d55-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="43d55-p108">Die beste Leistung erzielen Sie in einem Microsoft Access-Arbeitsbereich, insbesondere in einer Mehrbenutzerumgebung, indem Sie die **Execute**-Methode in einer Transaktion schachteln. Verwenden Sie die **BeginTrans**-Methode für das aktuelle **Workspace**-Objekt und dann die **Execute**-Methode. Schließen Sie die Transaktion mithilfe der **CommitTrans**-Methode für **Workspace** ab. Damit werden die Änderungen auf einem Datenträger gespeichert, und mögliche Sperren, die beim Ausführen der Abfrage angewendet wurden, werden aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="43d55-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

