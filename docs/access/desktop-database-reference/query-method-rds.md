---
title: Query-Methode (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e7f9dfc3ce5cb0d757951f13c1078ab44d04760
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949425"
---
# <a name="query-method-rds"></a><span data-ttu-id="78c39-102">Query-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="78c39-102">Query method (RDS)</span></span>

<span data-ttu-id="78c39-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78c39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78c39-104">Verwendet eine gültige SQL-Abfragezeichenfolge, um ein [Recordset](recordset-object-ado.md)-Objekt zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="78c39-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78c39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78c39-105">Syntax</span></span>

<span data-ttu-id="78c39-106">Festlegen von*Recordset-Objekt* = *DataFactory*. Abfrage (*Verbindung*, *Abfrage*)</span><span class="sxs-lookup"><span data-stu-id="78c39-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="78c39-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c39-107">Parameters</span></span>

|<span data-ttu-id="78c39-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78c39-108">Parameter</span></span>|<span data-ttu-id="78c39-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78c39-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="78c39-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="78c39-110">*Recordset*</span></span> |<span data-ttu-id="78c39-111">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="78c39-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="78c39-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="78c39-112">*DataFactory*</span></span> |<span data-ttu-id="78c39-113">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="78c39-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="78c39-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="78c39-114">*Connection*</span></span> |<span data-ttu-id="78c39-p101">Ein **String** -Wert, der die Informationen zur Serververbindung enthält. Er ist mit der [Connect](connect-property-rds.md)-Eigenschaft vergleichbar.</span><span class="sxs-lookup"><span data-stu-id="78c39-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="78c39-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="78c39-117">*Query*</span></span> |<span data-ttu-id="78c39-118">Ein **String**, der die SQL-Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="78c39-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="78c39-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78c39-119">Remarks</span></span>

<span data-ttu-id="78c39-p102">Für die Abfrage sollte der SQL-Dialekt des Datenbankservers verwendet werden. Tritt bei der ausgeführten Abfrage ein Fehler auf, wird ein Ergebnisstatus zurückgegeben. Die **Query** -Methode führt keine Syntaxüberprüfung für die **Query** -Zeichenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="78c39-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

