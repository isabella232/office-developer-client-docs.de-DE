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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="6ed2a-102">TRANSACTION-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6ed2a-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="6ed2a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ed2a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6ed2a-104">Wird zum Initiieren und Abschließen expliziter Transaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ed2a-105">Syntax</span></span>

<span data-ttu-id="6ed2a-106">Initiiert eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-106">Initiate a new transaction.</span></span>

<span data-ttu-id="6ed2a-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="6ed2a-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="6ed2a-108">Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="6ed2a-109">COMMIT \[Transaktion | ARBEIT\]</span><span class="sxs-lookup"><span data-stu-id="6ed2a-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="6ed2a-110">Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Rollback ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="6ed2a-111">ROLLBACK \[Transaktion | ARBEIT\]</span><span class="sxs-lookup"><span data-stu-id="6ed2a-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed2a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ed2a-112">Remarks</span></span>

<span data-ttu-id="6ed2a-p101">Transaktionen werden nicht automatisch gestartet. Zum Starten einer Transaktion müssen Sie explizit den Befehl BEGIN TRANSACTION verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="6ed2a-p102">Transaktionen können in bis zu fünf Ebenen geschachtelt sein. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="6ed2a-117">Für verknüpfte Tabellen werden Transaktionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed2a-117">Transactions are not supported for linked tables.</span></span>

