---
title: Database.Connection Property (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0974051b1f10fa73caad6d9feafb2e2b769579
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882840"
---
# <a name="databaseconnection-property-dao"></a>Database.Connection Property (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . Verbindung

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Rufen Sie mit der **Connection**-Eigenschaft einen Verweis auf das **Connection**-Objekt ab, das dem **Database**-Objekt entspricht. Bei DAO sind ein **Connection**-Objekt und dessen **Database**-Objekt einfach zwei verschiedene Objektvariablenverweise auf dasselbe Objekt. Mithilfe der **[Database](connection-database-property-dao.md)** -Eigenschaft eines **Connection**-Objekts und der **Connection**-Eigenschaft eines **Database**-Objekts können Verbindungen mit einer ODBC-Datenquelle über das Microsoft Access-Datenbankmodul leichter zur Verwendung von ODBCDirect geändert werden.

