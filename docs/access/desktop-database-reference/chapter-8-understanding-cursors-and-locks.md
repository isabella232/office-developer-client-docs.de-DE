---
title: 'Kapitel 8: Grundlegendes zu Cursorn und Sperren'
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99f363522874f01268f4c1a64515bf6f2cdd6336
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473608"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a>Kapitel 8: Grundlegendes zu Cursorn und Sperren


**Betrifft**: Access 2013 | Office 2013

Sie sollten unbedingt die Funktionsweise von Cursorn kennen, damit Sie den optimalen und effizientesten Cursortyp für die Datenzugriffsanforderungen einer Anwendung auswählen können. Durch eine nicht optimale Cursorkonfiguration können Datenzugriffsvorgänge extrem langsam werden.

Viele Funktionen des **Recordset** -ADO-Objekts werden durch den Cursortyp und die Cursorplatzierung sowie durch den Sperrtyp bestimmt.

In diesem Kapitel werden die folgenden Themen behandelt:

  - [Was ist ein Cursor?](what-is-a-cursor.md)

  - [Cursortypen](types-of-cursors.md)

  - [Bedeutung der Cursorplatzierung](the-significance-of-cursor-location.md)

  - [Microsoft Cursor Service für OLE DB](the-microsoft-cursor-service-for-ole-db.md)

  - [Was ist eine Sperre?](what-is-a-lock.md)

  - [Verwenden der CacheSize-Eigenschaft](using-cachesize.md)

  - [Merkmale von Cursorn und Sperren](cursor-and-lock-characteristics.md)

