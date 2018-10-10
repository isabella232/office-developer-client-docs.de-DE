---
title: StoppAlleMakros-Makroaktion
TOCTitle: StopAllMacros Macro Action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 80da04f7b5f99fd0b249164caaeaca9f25edd172
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472717"
---
# <a name="stopallmacros-macro-action"></a>StoppAlleMakros-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Verwenden Sie die **StoppAlleMakros** -Aktion, um alle laufenden Makros zu beenden.

## <a name="setting"></a>Einstellung

Die **StoppAlleMakros** -Aktion hat keine Argumente.

## <a name="remarks"></a>Hinweise

Normalerweise verwenden Sie diese Aktion, wenn eine Fehlersituation das Beenden aller Makros erfordert. Sie können einen bedingten Ausdruck in der Aktionszeile des Makros verwenden, die diese Aktion enthält. Wenn der Ausdruck auf **True** (– 1) ausgewertet wird, beendet Microsoft Access alle Makros.

Angenommen, ein Makro zeigt im Rahmen einer Reihe komplexer Aktionen, einschließlich der Ausführung weiterer Makros, ein Meldungsfeld an. Wenn der Benutzer in diesem Meldungsfeld auf **Abbrechen** klickt, kann die **StoppAlleMakros** -Aktion alle laufenden Makros beenden.

Wenn ein Makro die Aktionen **Echo** oder **Warnmeldungen** zum Ausschalten von Echo oder der Anzeige von Systemmeldungen verwendet hat, werden sie mit der **StoppAlleMakros** -Aktion wieder eingeschaltet.

Diese Aktion ist in einem VBA-Modul (Visual Basic für Applikationen) nicht verfügbar.

