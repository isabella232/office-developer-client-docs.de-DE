---
title: TRANSACTION-Anweisung (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474439"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

Wird zum Initiieren und Abschließen expliziter Transaktionen verwendet.

## <a name="syntax"></a>Syntax

Initiiert eine neue Transaktion.

BEGIN TRANSACTION

Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Commit ausgeführt wird.

COMMIT \[Transaktion | ARBEIT\]

Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Rollback ausgeführt wird.

ROLLBACK \[Transaktion | ARBEIT\]

## <a name="remarks"></a>Hinweise

Transaktionen werden nicht automatisch gestartet. Zum Starten einer Transaktion müssen Sie explizit den Befehl BEGIN TRANSACTION verwenden.

Transaktionen können in bis zu fünf Ebenen geschachtelt sein. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.

Für verknüpfte Tabellen werden Transaktionen nicht unterstützt.

