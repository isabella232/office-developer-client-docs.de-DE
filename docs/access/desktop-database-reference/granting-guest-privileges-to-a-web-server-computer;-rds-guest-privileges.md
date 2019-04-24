---
title: Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292125"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen

**Gilt für**: Access 2013, Office 2013

Das anonyme Webserverkonto (IUSR\_*Computername*) muss der lokalen Gruppe "Gäste" auf dem Webservercomputer hinzugefügt werden, um RDS verwenden zu können.

**So gewähren Sie einem Webservercomputer Gastberechtigungen**

1.  Klicken Sie auf dem Computer mit Microsoft Windows 2000-Server auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Computerverwaltung**.

2.  Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.

3.  Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.

4.  Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.

5.  Wenn das anonyme Webserverkonto nicht in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** angezeigt wird, geben Sie den Namen (IUSR\_*Computer*Name) in das untere leere Feld ein, und klicken Sie dann auf **Hinzufügen**.

6.  Klicken Sie auf **OK**.

