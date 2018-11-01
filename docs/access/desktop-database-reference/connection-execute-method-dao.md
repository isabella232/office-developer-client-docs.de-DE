---
title: Connection.Execute Method (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd7d0ec92643a8a177134e19ea3e40983efdbb11
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891198"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="f14a8-102">Connection.Execute Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="f14a8-102">Connection.Execute Method (DAO)</span></span>


<span data-ttu-id="f14a8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f14a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f14a8-104">Führt eine Aktionsabfrage oder eine SQL-Anweisung für das angegebene Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="f14a8-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f14a8-105">Syntax</span></span>

<span data-ttu-id="f14a8-106">*Ausdruck* . Führen Sie (***Abfrage***, ***Optionen***)</span><span class="sxs-lookup"><span data-stu-id="f14a8-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="f14a8-107">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f14a8-107">*expression* A variable that represents a **Connection** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f14a8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f14a8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f14a8-109">Name</span><span class="sxs-lookup"><span data-stu-id="f14a8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f14a8-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="f14a8-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f14a8-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f14a8-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f14a8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f14a8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f14a8-113">Abfrage</span><span class="sxs-lookup"><span data-stu-id="f14a8-113">Query</span></span></p></td>
<td><p><span data-ttu-id="f14a8-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f14a8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f14a8-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-116">Ein <strong>String</strong>-Wert, der eine SQL-Anweisung oder den <strong>Name</strong>-Eigenschaftswert eines <strong>QueryDef</strong>-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="f14a8-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14a8-117">Options</span><span class="sxs-lookup"><span data-stu-id="f14a8-117">Options</span></span></p></td>
<td><p><span data-ttu-id="f14a8-118">Optional</span><span class="sxs-lookup"><span data-stu-id="f14a8-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="f14a8-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-120">Eine Konstante oder eine Kombination aus Konstanten, durch die die Datenintegritätsmerkmale der Abfrage festgelegt sind, wie unter Einstellungen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f14a8-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f14a8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f14a8-121">Remarks</span></span>

<span data-ttu-id="f14a8-122">Sie können die folgenden **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)**-Konstanten für Optionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f14a8-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f14a8-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="f14a8-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="f14a8-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f14a8-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f14a8-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-126">Verweigert anderen Benutzern die Schreibberechtigung (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f14a8-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14a8-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-128">(Standardeinstellung) Führt inkonsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f14a8-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14a8-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-130">Führt konsistente Updates aus (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f14a8-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14a8-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-p101">Führt eine SQL-Pass-Through-Abfrage aus. Wenn Sie diese Option festlegen, wird die SQL-Anweisung zur Verarbeitung an eine ODBC-Datenbank übergeben (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f14a8-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14a8-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-135">Führt ein Rollback für Updates aus, wenn ein Fehler auftritt (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f14a8-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14a8-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-137">Generiert einen Laufzeitfehler, wenn ein anderer Benutzer Daten ändert, die Sie bearbeiten (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f14a8-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f14a8-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-139">Führt die Abfrage asynchron aus (nur ODBCDirect-Connection- und -QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="f14a8-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f14a8-140"><strong>Bei der Ausführung</strong></span><span class="sxs-lookup"><span data-stu-id="f14a8-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="f14a8-141">Führt die Anweisung aus, ohne zuvor die SQLPrepare ODBC-API-Funktion aufzurufen (nur ODBCDirect Connection- und QueryDef-Objekte).</span><span class="sxs-lookup"><span data-stu-id="f14a8-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f14a8-p102">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f14a8-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="f14a8-p103">[!HINWEIS] Die Konstanten **dbConsistent** und **dbInconsistent** schließen sich gegenseitig aus. Sie können eins von beiden, jedoch nicht beide in einer angegebenen Instanz von **OpenRecordset** verwenden. Durch die Verwendung der **dbConsistent** - und **dbInconsistent** -Konstanten wird ein Fehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="f14a8-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="f14a8-p104">Die **Execute**-Methode gilt nur für Aktionsabfragen. Wenn Sie **Execute** mit einem anderen Abfragetyp verwenden, tritt ein Fehler auf. Da bei einer Aktionsabfrage keine Datensätze zurückgegeben werden, gibt **Execute** kein **Recordset**-Objekt zurück. (Das Durchführen einer SQL Pass-Through-Abfrage in einem ODBCDirect-Arbeitsbereich gibt keinen Fehler zurück, wenn kein **Recordset** zurückgegeben wird.)</span><span class="sxs-lookup"><span data-stu-id="f14a8-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="f14a8-p105">Mit der **RecordsAffected**-Eigenschaft des **Connection**-, **Database**- oder **QueryDef**-Objekts können Sie die Anzahl von Datensätzen bestimmen, die von der aktuellsten **Execute**-Methode betroffen sind. So umfasst **RecordsAffected** beispielsweise die Anzahl von Datensätzen, die beim Ausführen einer Aktionsabfrage gelöscht, aktualisiert oder eingefügt wurden. Wenn Sie zum Ausführen einer Abfrage die **Execute**-Methode verwenden, ist die **RecordsAffected**-Eigenschaft des **QueryDef**-Objekts auf die Anzahl von betroffenen Datensätzen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f14a8-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="f14a8-p106">Wenn Sie in einem Microsoft Access-Arbeitsbereich eine syntaktisch richtige SQL-Anweisung angeben und über die entsprechenden Berechtigungen verfügen, schlägt die **Execute**-Methode nicht fehl, auch wenn keine einzelne Zeile geändert oder gelöscht werden kann. Daher sollten Sie immer mit der **dbFailOnError**-Option arbeiten, wenn Sie mit der **Execute**-Methode eine Aktualisierung ausführen oder eine Abfrage löschen. Mit dieser Option wird ein Laufzeitfehler generiert, und für alle erfolgreichen Änderungen wird ein Rollback durchgeführt, wenn einer der betroffenen Datensätze gesperrt ist und nicht aktualisiert oder gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f14a8-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="f14a8-p107">In früheren Versionen des Microsoft Jet-Datenbankmoduls wurden SQL-Anweisungen automatisch in implizite Transaktionen eingebettet. Würde ein Teil einer mit **dbFailOnError** ausgeführten Anweisung fehlschlagen, würde für die Anweisung ein Rollback durchgeführt. Zur Leistungssteigerung wurden diese impliziten Transaktionen ab Version 3.5 entfernt. Wenn Sie älteren DAO-Code aktualisieren, sollten Sie auf jeden Fall explizite Transaktionen bei **Execute**-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f14a8-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="f14a8-p108">Die beste Leistung erzielen Sie in einem Microsoft Access-Arbeitsbereich, insbesondere in einer Mehrbenutzerumgebung, indem Sie die **Execute**-Methode in einer Transaktion schachteln. Verwenden Sie die **BeginTrans**-Methode für das aktuelle **Workspace**-Objekt und dann die **Execute**-Methode. Schließen Sie die Transaktion mithilfe der **CommitTrans**-Methode für **Workspace** ab. Damit werden die Änderungen auf einem Datenträger gespeichert, und mögliche Sperren, die beim Ausführen der Abfrage angewendet wurden, werden aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="f14a8-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

