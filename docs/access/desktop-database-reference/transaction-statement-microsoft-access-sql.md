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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="46360-102">TRANSACTION-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="46360-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="46360-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46360-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46360-104">Dient zum Auslösen und Abschließen expliziter Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="46360-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="46360-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46360-105">Syntax</span></span>

<span data-ttu-id="46360-106">**Initiiert eine neue Transaktion**:</span><span class="sxs-lookup"><span data-stu-id="46360-106">Initiate a new transaction.</span></span>

<span data-ttu-id="46360-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="46360-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="46360-108">**Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Commit ausgeführt wird**:</span><span class="sxs-lookup"><span data-stu-id="46360-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="46360-109">COMMIT \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="46360-109">COMMIT [TRANSACTION | WORK]</span></span>

<span data-ttu-id="46360-110">**Schließt eine Transaktion ab, indem für alle während der Transaktion ausgeführten Schritte ein Rollback ausgeführt wird**:</span><span class="sxs-lookup"><span data-stu-id="46360-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="46360-111">ROLLBACK \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="46360-111">ROLLBACK [TRANSACTION | WORK]</span></span>

## <a name="remarks"></a><span data-ttu-id="46360-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46360-112">Remarks</span></span>

<span data-ttu-id="46360-p101">Transaktionen werden nicht automatisch gestartet. Um eine Transaktion zu starten, müssen Sie dazu BEGIN TRANSACTION explizit verwenden.</span><span class="sxs-lookup"><span data-stu-id="46360-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="46360-p102">Transaktionen können bis zu fünf Ebenen tief geschachtelt werden. Zum Starten einer geschachtelten Transaktion verwenden Sie BEGIN TRANSACTION im Kontext einer vorhandenen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="46360-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="46360-117">Transaktionen werden nicht für verknüpfte Tabellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46360-117">Transactions are not supported for linked tables.</span></span>

