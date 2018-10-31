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
ms.openlocfilehash: 6d93fc90beded30d96b4db54c35ab3046da06899
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862664"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Wird zum Initiieren und Abschließen expliziter Transaktionen verwendet.

## <a name="syntax"></a>Syntax

**Initiiert eine neue Transaktion**:

BEGIN TRANSACTION

**Während der Transaktion ausgeführten Conclude eine Transaktion, indem ein Commit für alle arbeiten**:

COMMIT \[Transaktion | ARBEIT\]

**Conclude einer Transaktion, indem ein Rollback alle Arbeit während der Transaktion ausgeführten**:

ROLLBACK \[Transaktion | ARBEIT\]

## <a name="remarks"></a>Hinweise

Transaktionen werden nicht automatisch gestartet. Zum Starten einer Transaktion müssen Sie explizit den Befehl BEGIN TRANSACTION verwenden.

Transaktionen können in bis zu fünf Ebenen geschachtelt sein. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.

Für verknüpfte Tabellen werden Transaktionen nicht unterstützt.

