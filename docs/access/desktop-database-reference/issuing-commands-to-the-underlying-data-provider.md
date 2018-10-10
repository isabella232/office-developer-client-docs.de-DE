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
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Ausstellen von Befehlen für den zugrunde liegenden Datenprovider


**Betrifft**: Access 2013 | Office 2013

Jeder Befehl, der nicht mit SHAPE beginnt, wird an den Datenprovider übergeben. Dies entspricht dem Ausstellen eines SHAPE-Befehls im Format "SHAPE {Providerbefehl}". Führen Sie diese Befehle *nicht* haben, um ein **Recordset-Objekt**zu erstellen. Beispielsweise ist "SHAPE {DROP TABLE MyTable}" ein absolut gültiger SHAPE-Befehl, vorausgesetzt der Datenprovider unterstützt DROP TABLE.

Aufgrund dieser Funktion können normale Providerbefehle und SHAPE-Befehle die gleiche Verbindung und Transaktion verwenden.

