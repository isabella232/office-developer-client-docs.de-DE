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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291088"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="941d9-102">Ausgabe von Befehlen an den zugrunde liegenden Datenanbieter</span><span class="sxs-lookup"><span data-stu-id="941d9-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="941d9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="941d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="941d9-p101">Jeder Befehl, der nicht mit SHAPE beginnt, wird an den Datenprovider übergeben. Dies entspricht dem Ausstellen eines SHAPE-Befehls im Format "SHAPE {Providerbefehl}". Diese Befehle müssen \*kein \***Recordset**-Objekt erzeugen. Beispielsweise ist "SHAPE {DROP TABLE MyTable}" ein absolut gültiger SHAPE-Befehl, vorausgesetzt der Datenprovider unterstützt DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="941d9-p101">Any command that does not begin with SHAPE is passed through to the data provider. This is equivalent to issuing a shape command in the form "SHAPE {provider command}". These commands do *not* have to produce a **Recordset**. For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="941d9-108">Aufgrund dieser Funktion können normale Providerbefehle und SHAPE-Befehle die gleiche Verbindung und Transaktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="941d9-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

