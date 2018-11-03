---
title: Ausstellen von Befehlen für den zugrunde liegenden Datenprovider
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 142772aaff5080a6e2522ab31884f2ff2319c8a7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944634"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="05deb-102">Ausstellen von Befehlen für den zugrunde liegenden Datenprovider</span><span class="sxs-lookup"><span data-stu-id="05deb-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="05deb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05deb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05deb-104">Jeder Befehl, der nicht mit SHAPE beginnt, wird an den Datenprovider übergeben.</span><span class="sxs-lookup"><span data-stu-id="05deb-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="05deb-105">Dies entspricht dem Ausstellen eines SHAPE-Befehls im Format "SHAPE {Providerbefehl}".</span><span class="sxs-lookup"><span data-stu-id="05deb-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="05deb-106">Führen Sie diese Befehle *nicht* haben, um ein **Recordset-Objekt**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="05deb-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="05deb-107">Beispielsweise ist "SHAPE {DROP TABLE MyTable}" ein absolut gültiger SHAPE-Befehl, vorausgesetzt der Datenprovider unterstützt DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="05deb-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="05deb-108">Aufgrund dieser Funktion können normale Providerbefehle und SHAPE-Befehle die gleiche Verbindung und Transaktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="05deb-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

