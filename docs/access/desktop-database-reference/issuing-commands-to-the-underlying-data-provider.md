---
title: Ausstellen von Befehlen für den zugrunde liegenden Datenprovider
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473728"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="f21d2-102">Ausstellen von Befehlen für den zugrunde liegenden Datenprovider</span><span class="sxs-lookup"><span data-stu-id="f21d2-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="f21d2-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f21d2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f21d2-104">Jeder Befehl, der nicht mit SHAPE beginnt, wird an den Datenprovider übergeben.</span><span class="sxs-lookup"><span data-stu-id="f21d2-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="f21d2-105">Dies entspricht dem Ausstellen eines SHAPE-Befehls im Format "SHAPE {Providerbefehl}".</span><span class="sxs-lookup"><span data-stu-id="f21d2-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="f21d2-106">Führen Sie diese Befehle *nicht* haben, um ein **Recordset-Objekt**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f21d2-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="f21d2-107">Beispielsweise ist "SHAPE {DROP TABLE MyTable}" ein absolut gültiger SHAPE-Befehl, vorausgesetzt der Datenprovider unterstützt DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="f21d2-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="f21d2-108">Aufgrund dieser Funktion können normale Providerbefehle und SHAPE-Befehle die gleiche Verbindung und Transaktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="f21d2-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

