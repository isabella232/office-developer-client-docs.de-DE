---
title: Anpassen der Einstellungen in der Windows-Registrierung für das Microsoft Access-Datenbankmodul
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 99e2b31cf686895a56e9d70b177314355c1aff3c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945146"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Anpassen der Einstellungen in der Windows-Registrierung für das Microsoft Access-Datenbankmodul

**Betrifft**: Access 2013, Office 2013

Wenn die Anwendung mit der Standardfunktionalität von Microsoft Access-Datenbankmodul ordnungsgemäß arbeiten kann, müssen Sie möglicherweise die Einstellungen in der Microsoft Windows-Registrierung nach Bedarf ändern. Mithilfe der Windows-Registrierung können Sie auch die Arbeitsweise der installierbaren ISAM- nd ODBC-Treiber optimieren.

Es gibt vier verschiedene Möglichkeiten, die Einstellungen in der Windows-Registrierung anzupassen:

- [Mithilfe von Regedit.exe, um die Standardeinstellungen zu überschreiben.](https://msdn.microsoft.com/library/ff193205\(v=office.15\))
- [Erstellen eines Teils im Registrierungsbaum Ihrer Anwendung, zum Verwalten der Einstellungen](https://msdn.microsoft.com/library/ff836342\(v=office.15\))
- [Verwenden der SetOption-Methode von DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))
- [Verwenden der Verbindungseigenschaften im Microsoft OLE DB Provider für Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))

