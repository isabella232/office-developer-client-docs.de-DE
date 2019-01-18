---
title: Ausgabe von Befehlen an den zugrunde liegenden Datenanbieter
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709614"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="565ef-102">Ausgabe von Befehlen an den zugrunde liegenden Datenanbieter</span><span class="sxs-lookup"><span data-stu-id="565ef-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="565ef-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="565ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="565ef-104">Jeder Befehl, der nicht mit SHAPE beginnt, wird an den Datenprovider übergeben.</span><span class="sxs-lookup"><span data-stu-id="565ef-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="565ef-105">Dies entspricht dem Ausstellen eines SHAPE-Befehls im Format "SHAPE {Providerbefehl}".</span><span class="sxs-lookup"><span data-stu-id="565ef-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="565ef-106">Führen Sie diese Befehle *nicht* haben, um ein **Recordset-Objekt**zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="565ef-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="565ef-107">Beispielsweise ist "SHAPE {DROP TABLE MyTable}" ein absolut gültiger SHAPE-Befehl, vorausgesetzt der Datenprovider unterstützt DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="565ef-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="565ef-108">Aufgrund dieser Funktion können normale Providerbefehle und SHAPE-Befehle die gleiche Verbindung und Transaktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="565ef-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

