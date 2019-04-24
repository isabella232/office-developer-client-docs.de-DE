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
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314147"
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

