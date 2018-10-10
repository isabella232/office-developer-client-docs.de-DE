---
title: Verwenden der AddNew-Methode im sofortigen Aktualisierungsmodus und im Batchmodus
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b37acc1819d12acc1e659be85361c3c09b84ebdb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473681"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Verwenden der AddNew-Methode im sofortigen Aktualisierungsmodus und im Batchmodus


**Betrifft**: Access 2013 | Office 2013

Das Verhalten der **AddNew** -Methode hängt vom Aktualisierungsmodus des **Recordset** -Objekts und gibt an, ob Sie die Argumente *FieldList* und *Values* übergeben.

Im sofortigen Aktualisierungsmodus (bei dem der Anbieter Änderungen in die zugrunde liegende Datenquelle schreibt, wenn Sie die **Update**-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die **EditMode**-Eigenschaft auf **adEditAdd** festgelegt. Änderungen der Werte von Feldern werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz in der Datenbank bereitgestellt, und die **EditMode**-Eigenschaft wird auf **adEditNone** zurückgesetzt. Wenn Sie die Argumente *FieldList* und *Values* übergeben, stellt ADO den neuen Datensatz sofort in der Datenbank bereit (der Aufruf von **Update** ist nicht erforderlich). Der Wert der **EditMode**-Eigenschaft wird nicht geändert (**adEditNone**).

Aufrufen der **AddNew** -Methode ohne Argumente im Batchaktualisierungsmodus werden die **EditMode** -Eigenschaft auf **AdEditAdd**festgelegt. Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert. Aufrufen der **Update** -Methode fügt den neuen Datensatz zum aktuellen **Recordset-Objekt** und die **EditMode** -Eigenschaft auf **adEditNone festgelegt**, aber der Anbieter nicht die Änderungen an der zugrunde liegenden Datenbank gebucht wird erst nach dem Aufruf der **UpdateBatch **Methode. Wenn Sie die Argumente *FieldList* und *Values* übergeben, sendet ADO den neuen Datensatz an den Anbieter für die Speicherung in einem Cache. Sie müssen die **UpdateBatch** -Methode, um den neuen Datensatz in der zugrunde liegenden Datenbank buchen aufrufen. Weitere Informationen zu **Updates** und **UpdateBatch**, finden Sie unter [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

