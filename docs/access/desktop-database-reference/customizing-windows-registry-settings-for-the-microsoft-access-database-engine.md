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
ms.localizationpriority: medium
ms.openlocfilehash: d50bb27baca6c7f340fbafcc55f44e56ded1dcf1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558548"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a>Anpassen der Einstellungen in der Windows-Registrierung für das Microsoft Access-Datenbankmodul

**Gilt für**: Access 2013, Office 2013

Wenn Ihre Anwendung mit der Standardfunktionalität des Microsoft Access-Datenbankmoduls nicht ordnungsgemäß funktioniert, müssen Sie möglicherweise die Einstellungen in der Microsoft Windows-Registrierung entsprechend Ihren Anforderungen ändern. Mithilfe der Windows-Registrierung können Sie auch die Arbeitsweise der installierbaren ISAM- nd ODBC-Treiber optimieren.

Es gibt vier verschiedene Möglichkeiten, die Einstellungen in der Windows-Registrierung anzupassen:

- [Verwenden von Regedit.exe zum Überschreiben der Standardeinstellungen](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [Erstellen eines Teils in der Registrierungsstruktur Ihrer Anwendung zum Verwalten der Einstellungen](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [Verwenden der SetOption-Methode von DAO](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [Verwenden der Connection-Eigenschaften im Microsoft OLE DB-Anbieter für Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

