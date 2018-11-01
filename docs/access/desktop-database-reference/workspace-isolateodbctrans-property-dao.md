---
title: Workspace.IsolateODBCTrans Property (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 197bf35c796fe1e34122b7d4214043e9217fb3d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878542"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Workspace.IsolateODBCTrans Property (DAO)


**Betrifft**: Access 2013, Office 2013

Legt einen Wert fest, der angibt, ob mehrere Transaktionen, die dieselbe mit der Microsoft Access-Datenbank-Engine verbundene ODBC-Datenquelle verwenden, isoliert sind, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . IsolateODBCTrans

*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Es gibt Situationen, in denen mehrere gleichzeitige Transaktionen für dieselbe ODBC-Verbindung zur Verarbeitung anstehen müssen. Hierzu müssen Sie für jede Transaktion ein eigenes **Workspace**-Objekt öffnen. Wenngleich jedes **Workspace**-Objekt seine eigene ODBC-Verbindung zur Datenbank haben kann, wird dadurch die Systemleistung beeinträchtigt. Da gewöhnlich keine Transaktionsisolation erforderlich ist, können ODBC-Verbindungen von mehreren **Workspace**-Objekten, die von einem Benutzer geöffnet wurden, standardmäßig gemeinsam verwendet werden.

Einige ODBC-Server, wie etwa Microsoft SQL Server, gestatten keine gleichzeitigen Transaktionen über eine einzelne Verbindung. Wenn in einer solchen Datenbank mehrere Transaktionen gleichzeitig ausstehen, legen Sie für jedes **Workspace**-Objekt sofort nach dem Öffnen den Wert der **IsolateODBCTrans**-Eigenschaft auf **True** fest. Dadurch wird für jedes **Workspace**-Objekt eine separate ODBC-Verbindung erzwungen.

