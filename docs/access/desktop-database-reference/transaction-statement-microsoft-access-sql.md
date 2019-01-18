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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705519"
---
# <a name="transaction-statement-microsoft-access-sql"></a>TRANSACTION-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

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

