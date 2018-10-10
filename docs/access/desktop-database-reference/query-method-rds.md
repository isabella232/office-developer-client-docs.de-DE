---
title: Query-Methode (RDS - Access-desktop-Datenbank (engl.))
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9a9ecb2d7ebfdd8f6738b8d7b9b8738ce981ec16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473115"
---
# <a name="query-method-rds"></a>Query-Methode (RDS)


**Betrifft**: Access 2013 | Office 2013


Verwendet eine gültige SQL-Abfragezeichenfolge, um ein [Recordset](recordset-object-ado.md)-Objekt zurückzugeben.

## <a name="syntax"></a>Syntax

Festlegen von*Recordset-Objekt* = *DataFactory*. Abfrage (*Verbindung*, *Abfrage*)

## <a name="parameters"></a>Parameter

  - *Recordset*

  - Eine Objektvariable, die ein **Recordset** -Objekt darstellt.

  - *DataFactory*

  - Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.

  - *Connection*

  - Ein **String** -Wert, der die Informationen zur Serververbindung enthält. Er ist mit der [Connect](connect-property-rds.md)-Eigenschaft vergleichbar.

  - *Query*

  - Ein **String**, der die SQL-Abfrage enthält.

## <a name="remarks"></a>Hinweise

Für die Abfrage sollte der SQL-Dialekt des Datenbankservers verwendet werden. Tritt bei der ausgeführten Abfrage ein Fehler auf, wird ein Ergebnisstatus zurückgegeben. Die **Query** -Methode führt keine Syntaxüberprüfung für die **Query** -Zeichenfolge aus.

