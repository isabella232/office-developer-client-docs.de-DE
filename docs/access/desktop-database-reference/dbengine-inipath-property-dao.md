---
title: DBEngine.IniPath Property (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 344f5b0a1edac379386208a831d332e8926654ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882959"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath Property (DAO)


**Betrifft**: Access 2013, Office 2013

Legt Informationen über den Windows-Registrierungsschlüssel fest, der Werte für die Microsoft Access-Datenbank-Engine enthält, oder gibt die Informationen zurück (nur Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . IniPath

*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Sie können die Microsoft Access-Datenbank-Engine mit der Windows-Registrierung konfigurieren. Mit der Registrierung können Sie Optionen festlegen, wie etwa installierbare ISAM-DLL-Dateien.

Damit diese Option wirksam wird, müssen Sie die **IniPath**-Eigenschaft festlegen, bevor Ihre Anwendung einen anderen DAO-Code aufruft. Die Wirkung dieser Einstellung ist auf die Anwendung begrenzt. Sie kann nur geändert werden, wenn Sie die Anwendung neu starten.

Die Registrierung dient auch zur Bereitstellung von Initialisierungsparametern für einige installierbare ISAM-Datenbanktreiber. Beispiel: Zur Verwendung von Paradox Version 4.0 legen Sie für die **IniPath**-Eigenschaft den Teil der Registrierung fest, der die betreffenden Parameter enthält.

Diese Eigenschaft erkennt entweder HKEY\_lokale\_Computer oder HKEY\_lokale\_Benutzer. Wenn kein Stammschlüssel bereitgestellt wird, wird der Standardwert ist HKEY\_lokale\_Computer.

