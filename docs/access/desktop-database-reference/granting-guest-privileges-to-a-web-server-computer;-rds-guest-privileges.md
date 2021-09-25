---
title: Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: df3b2043dbfc9fe09b842f999db3e40f5e5ec2b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577325"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen

**Gilt für**: Access 2013, Office 2013

Das anonyme Webserverkonto (IUSR \_ *ComputerName)* muss der lokalen Gruppe "Gäste" auf dem Webservercomputer hinzugefügt werden, um RDS zu verwenden.

**So gewähren Sie einem Webservercomputer Gastberechtigungen**

1.  Klicken Sie auf Ihrem Computer mit Microsoft Windows 2000 Server auf **"Start",** **"Programme",** **"Auf Verwaltungstools"** und dann auf **"Computerverwaltung".**

2.  Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.

3.  Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.

4.  Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.

5.  Wenn das anonyme Webserverkonto nicht in der Liste im Dialogfeld Benutzer **oder Gruppen auswählen** angezeigt wird, geben Sie seinen Namen (IUSR \_ *ComputerName)* in das untere leere Feld ein, und klicken Sie dann auf **Hinzufügen**.

6.  Klicken Sie auf **OK**.

