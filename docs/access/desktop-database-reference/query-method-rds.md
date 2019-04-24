---
title: Query-Methode (RDS-Access-Desktop-Daten Bankreferenz)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301113"
---
# <a name="query-method-rds"></a>Query-Methode (RDS)

**Gilt für**: Access 2013, Office 2013

Verwendet eine gültige SQL-Abfragezeichenfolge, um ein [Recordset](recordset-object-ado.md)-Objekt zurückzugeben.

## <a name="syntax"></a>Syntax

*Recordset* = -Daten*Factory*festlegen. Abfrage (*Verbindung*, *Abfrage*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Recordset* |Eine Objektvariable, die ein **Recordset** -Objekt darstellt.|
|*DataFactory* |Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.|
|*Connection* |Ein **String** -Wert, der die Informationen zur Serververbindung enthält. Er ist mit der [Connect](connect-property-rds.md)-Eigenschaft vergleichbar.|
|*Query* |Ein **String**, der die SQL-Abfrage enthält.|

## <a name="remarks"></a>Bemerkungen

Für die Abfrage sollte der SQL-Dialekt des Datenbankservers verwendet werden. Tritt bei der ausgeführten Abfrage ein Fehler auf, wird ein Ergebnisstatus zurückgegeben. Die **Query**-Methode führt keine Syntaxüberprüfung für die **Query**-Zeichenfolge aus.

