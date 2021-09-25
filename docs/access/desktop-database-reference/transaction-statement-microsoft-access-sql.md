---
title: TRANSACTION-Anweisung (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: e3ed36a0805754f15527b476528d875fa4844dcf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601646"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Dient zum Auslösen und Abschließen expliziter Transaktionen.

## <a name="syntax"></a>Syntax

**Initiiert eine neue Transaktion**:

BEGIN TRANSACTION

**Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Commit ausgeführt wird**:

COMMIT \[TRANSACTION | WORK\]

**Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Rollback ausgeführt wird**:

ROLLBACK \[TRANSACTION | WORK\]

## <a name="remarks"></a>Bemerkungen

Transaktionen werden nicht automatisch gestartet. Um eine Transaktion zu starten, müssen Sie dazu BEGIN TRANSACTION explizit verwenden.

Transaktionen können bis zu fünf Ebenen tief geschachtelt werden. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.

Transaktionen werden nicht für verknüpfte Tabellen unterstützt.

