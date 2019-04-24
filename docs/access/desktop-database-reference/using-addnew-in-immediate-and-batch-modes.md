---
title: Verwenden der AddNew-Methode im sofortigen Aktualisierungsmodus und im Batchmodus
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312754"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Verwenden von AddNew im sofort-und Batch Modus


**Gilt für**: Access 2013, Office 2013

Das Verhalten der **AddNew**-Methode hängt ab vom Aktualisierungsmodus des **Recordset**-Objekts und ob Sie die Argumente *FieldList* und *Values* übergeben.

Im sofortigen Aktualisierungsmodus (bei dem der Anbieter Änderungen in die zugrunde liegende Datenquelle schreibt, wenn Sie die **Update**-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die **EditMode**-Eigenschaft auf **adEditAdd** festgelegt. Änderungen der Werte von Feldern werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz in der Datenbank bereitgestellt, und die **EditMode**-Eigenschaft wird auf **adEditNone** zurückgesetzt. Wenn Sie die Argumente *FieldList* und *Values* übergeben, stellt ADO den neuen Datensatz sofort in der Datenbank bereit (der Aufruf von **Update** ist nicht erforderlich). Der Wert der **EditMode**-Eigenschaft wird nicht geändert (**adEditNone**).

Im Batchaktualisierungsmodus wird durch Aufrufen der **AddNew**-Methode ohne Argumente die **EditMode**-Eigenschaft auf **adEditAdd** festgelegt. Änderungen der Werte von Feldern werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz dem aktuellen **Recordset**-Objekt hinzugefügt, und die **EditMode**-Eigenschaft wird auf **adEditNone** zurückgesetzt. Die Änderungen werden jedoch vom Anbieter erst in der zugrunde liegenden Datenbank bereitgestellt, wenn Sie die **UpdateBatch**-Methode aufrufen. Wenn Sie die Argumente *FieldList* und *Values* übergeben, sendet ADO den neuen Datensatz an den Anbieter, um ihn in einem Cache zu speichern. Sie müssen die **UpdateBatch**-Methode aufrufen, um den neuen Datensatz in der zugrunde liegenden Datenbank bereitzustellen. Weitere Informationen zu **Update** und **UpdateBatch** finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

