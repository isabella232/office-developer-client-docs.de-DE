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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="1c0a8-102">TRANSACTION-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1c0a8-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="1c0a8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c0a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c0a8-104">Wird zum Initiieren und Abschließen expliziter Transaktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c0a8-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c0a8-105">Syntax</span></span>

<span data-ttu-id="1c0a8-106">**Initiiert eine neue Transaktion**:</span><span class="sxs-lookup"><span data-stu-id="1c0a8-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="1c0a8-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="1c0a8-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="1c0a8-108">**Während der Transaktion ausgeführten Conclude eine Transaktion, indem ein Commit für alle arbeiten**:</span><span class="sxs-lookup"><span data-stu-id="1c0a8-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="1c0a8-109">COMMIT \[Transaktion | ARBEIT\]</span><span class="sxs-lookup"><span data-stu-id="1c0a8-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="1c0a8-110">**Conclude einer Transaktion, indem ein Rollback alle Arbeit während der Transaktion ausgeführten**:</span><span class="sxs-lookup"><span data-stu-id="1c0a8-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="1c0a8-111">ROLLBACK \[Transaktion | ARBEIT\]</span><span class="sxs-lookup"><span data-stu-id="1c0a8-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="1c0a8-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c0a8-112">Remarks</span></span>

<span data-ttu-id="1c0a8-p101">Transaktionen werden nicht automatisch gestartet. Zum Starten einer Transaktion müssen Sie explizit den Befehl BEGIN TRANSACTION verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c0a8-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="1c0a8-p102">Transaktionen können in bis zu fünf Ebenen geschachtelt sein. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="1c0a8-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="1c0a8-117">Für verknüpfte Tabellen werden Transaktionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1c0a8-117">Transactions are not supported for linked tables.</span></span>

