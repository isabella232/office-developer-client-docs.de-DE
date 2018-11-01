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
ms.openlocfilehash: f48b1ab98f6f0f729fdb32b4ff20be09c5d942bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886389"
---
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="b1551-102">TRANSACTION-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b1551-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b1551-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1551-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1551-104">Wird zum Initiieren und Abschließen expliziter Transaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1551-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1551-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1551-105">Syntax</span></span>

<span data-ttu-id="b1551-106">**Initiiert eine neue Transaktion**:</span><span class="sxs-lookup"><span data-stu-id="b1551-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="b1551-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="b1551-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="b1551-108">**Während der Transaktion ausgeführten Conclude eine Transaktion, indem ein Commit für alle arbeiten**:</span><span class="sxs-lookup"><span data-stu-id="b1551-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="b1551-109">COMMIT \[Transaktion | ARBEIT\]</span><span class="sxs-lookup"><span data-stu-id="b1551-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="b1551-110">**Conclude einer Transaktion, indem ein Rollback alle Arbeit während der Transaktion ausgeführten**:</span><span class="sxs-lookup"><span data-stu-id="b1551-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="b1551-111">ROLLBACK \[Transaktion | ARBEIT\]</span><span class="sxs-lookup"><span data-stu-id="b1551-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="b1551-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1551-112">Remarks</span></span>

<span data-ttu-id="b1551-p101">Transaktionen werden nicht automatisch gestartet. Zum Starten einer Transaktion müssen Sie explizit den Befehl BEGIN TRANSACTION verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1551-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="b1551-p102">Transaktionen können in bis zu fünf Ebenen geschachtelt sein. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="b1551-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="b1551-117">Für verknüpfte Tabellen werden Transaktionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1551-117">Transactions are not supported for linked tables.</span></span>

