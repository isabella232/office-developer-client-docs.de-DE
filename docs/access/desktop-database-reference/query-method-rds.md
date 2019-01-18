---
title: Query-Methode (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717356"
---
# <a name="query-method-rds"></a><span data-ttu-id="24d24-102">Query-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="24d24-102">Query method (RDS)</span></span>

<span data-ttu-id="24d24-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="24d24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24d24-104">Verwendet eine gültige SQL-Abfragezeichenfolge, um ein [Recordset](recordset-object-ado.md)-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="24d24-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="24d24-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24d24-105">Syntax</span></span>

<span data-ttu-id="24d24-106">Festlegen von*Recordset-Objekt* = *DataFactory*. Abfrage (*Verbindung*, *Abfrage*)</span><span class="sxs-lookup"><span data-stu-id="24d24-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="24d24-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d24-107">Parameters</span></span>

|<span data-ttu-id="24d24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="24d24-108">Parameter</span></span>|<span data-ttu-id="24d24-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24d24-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="24d24-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="24d24-110">*Recordset*</span></span> |<span data-ttu-id="24d24-111">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="24d24-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="24d24-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="24d24-112">*DataFactory*</span></span> |<span data-ttu-id="24d24-113">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="24d24-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="24d24-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="24d24-114">*Connection*</span></span> |<span data-ttu-id="24d24-p101">Ein **String** -Wert, der die Informationen zur Serververbindung enthält. Er ist mit der [Connect](connect-property-rds.md)-Eigenschaft vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="24d24-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="24d24-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="24d24-117">*Query*</span></span> |<span data-ttu-id="24d24-118">Ein **String**, der die SQL-Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="24d24-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="24d24-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24d24-119">Remarks</span></span>

<span data-ttu-id="24d24-p102">Für die Abfrage sollte der SQL-Dialekt des Datenbankservers verwendet werden. Tritt bei der ausgeführten Abfrage ein Fehler auf, wird ein Ergebnisstatus zurückgegeben. Die **Query** -Methode führt keine Syntaxüberprüfung für die **Query** -Zeichenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="24d24-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

