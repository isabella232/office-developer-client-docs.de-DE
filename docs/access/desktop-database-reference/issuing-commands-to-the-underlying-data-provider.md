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
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Ausstellen von Befehlen für den zugrunde liegenden Datenprovider

**Betrifft**: Access 2013, Office 2013

Jeder Befehl, der nicht mit SHAPE beginnt, wird an den Datenprovider übergeben. Dies entspricht dem Ausstellen eines SHAPE-Befehls im Format "SHAPE {Providerbefehl}". Führen Sie diese Befehle *nicht* haben, um ein **Recordset-Objekt**zu erstellen. Beispielsweise ist "SHAPE {DROP TABLE MyTable}" ein absolut gültiger SHAPE-Befehl, vorausgesetzt der Datenprovider unterstützt DROP TABLE.

Aufgrund dieser Funktion können normale Providerbefehle und SHAPE-Befehle die gleiche Verbindung und Transaktion verwenden.

