---
title: Database.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5676ad0289891fad442e5670fc0d3d9c8d769419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618266"
---
# <a name="databaseclose-method-dao"></a>Database.Close-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Schließt ein geöffnetes **Database**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* .Close

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **Database**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Eine Alternative zur **Close**-Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).

