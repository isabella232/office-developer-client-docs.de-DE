---
title: Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed450913c7512e8ef20983484ca4b874878fd791
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867167"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen 


**Betrifft**: Access 2013, Office 2013

Das anonyme Webserverkonto (IUSR\_*ComputerName*) der lokalen Gruppe Gäste auf dem Webservercomputer Verwendung von RDS hinzugefügt werden müssen

**So erteilen einem Webservercomputer Gastberechtigungen**

1.  Klicken Sie auf dem Computer unter Microsoft Windows® 2000 Server auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Computerverwaltung**.

2.  Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.

3.  Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.

4.  Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.

5.  Wenn das anonyme Webserverkonto in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** nicht angezeigt wird, geben Sie deren Namen (IUSR\_*ComputerName*) in der unteren leer Feld, und klicken Sie dann auf **Hinzufügen**.

6.  Klicken Sie auf **OK**.

