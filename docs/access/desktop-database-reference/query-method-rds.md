---
title: Abfragemethode (RDS – Access-Desktopdatenbankreferenz)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 965dbe7736483c6e2cc926ec4f9fc037e503089b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562426"
---
# <a name="query-method-rds"></a>Query-Methode (RDS)

**Gilt für**: Access 2013, Office 2013

Verwendet eine gültige SQL-Abfragezeichenfolge, um ein [Recordset](recordset-object-ado.md)-Objekt zurückzugeben.

## <a name="syntax"></a>Syntax

Set *Recordset*  =  *DataFactory*. Query(*Connection*, *Query*)

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Recordset* |Eine Objektvariable, die ein **Recordset** -Objekt darstellt.|
|*DataFactory* |Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.|
|*Connection* |Ein **String** -Wert, der die Informationen zur Serververbindung enthält. Er ist mit der [Connect](connect-property-rds.md)-Eigenschaft vergleichbar.|
|*Query* |Ein **String**, der die SQL-Abfrage enthält.|

## <a name="remarks"></a>HinwBemerkungeneise

Für die Abfrage sollte der SQL-Dialekt des Datenbankservers verwendet werden. Tritt bei der ausgeführten Abfrage ein Fehler auf, wird ein Ergebnisstatus zurückgegeben. Die **Query**-Methode führt keine Syntaxüberprüfung für die **Query**-Zeichenfolge aus.

