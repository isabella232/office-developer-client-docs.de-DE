---
title: MinimierenFenster-Makroaktion
TOCTitle: MinimizeWindow Macro Action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8ff22b21bfc411f536b780d74a0c2b62a396a4cf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476155"
---
# <a name="minimizewindow-macro-action"></a>MinimierenFenster-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Wenn überlappende Fenster anstelle von Dokumente im Registerkartenformat verwenden Zugriff konfiguriert ist, können Sie die **Minimierenfenster** -Aktion verwenden, um das aktive Fenster auf eine kleine Titelleiste am unteren Rand des Access-Fensters zu reduzieren.


> [!NOTE]
> <P>[!HINWEIS] Diese Aktion kann auf Codefenster des Visual Basic-Editors nicht angewendet werden. Informationen zu den Auswirkungen auf Codefenster finden Sie im Thema zur <STRONG>WindowState</STRONG> -Eigenschaft.</P>



## <a name="setting"></a>Einstellung

Die **MinimierenFenster** -Aktion hat keine Argumente.

## <a name="remarks"></a>Hinweise

Sie können diese Aktion verwenden, um ein Fenster vom Bildschirm zu entfernen, während das Objekt geöffnet bleibt. Sie können diese Aktion auch verwenden, um ein Objekt zu öffnen, ohne sein Fenster anzuzeigen. Zum Anzeigen des Objekts verwenden Sie die **AuswählenObjekt** -Aktion mit der Aktion **MaximierenFenster** oder **WiederherstellenFenster**. Durch die **WiederherstellenFenster** -Aktion wird ein minimiertes Fenster in seiner vorherigen Größe wiederhergestellt.

Die **Minimierenfenster** -Aktion hat dieselbe Wirkung wie das Klicken auf die Schaltfläche **Minimieren** in der oberen rechten Fensterecke oder klicken auf **Minimieren** im **Systemmenü des Fensters** .

**Tipps**

  - Wenn das Fenster, das Sie minimieren möchten, nicht das aktive Fenster ist, müssen Sie zuerst die **AuswählenObjekt** -Aktion verwenden.

  - Wenn Sie den Navigationsbereich ausblenden möchten, müssen Sie zuerst die AuswählenObjekt-Aktion mit der Einstellung Ja für das Argument Im Datenbankfenster und anschließend die MinimierenFenster-Aktion verwenden. Das Objekt, das Sie in der AuswählenObjekt-Aktion auswählen, kann ein beliebiges Objekt in der Datenbank sein.

  - Sie können das aktive Fenster ausblenden, indem Sie auf im Menü **Ansicht** auf **Dieses Fenster verwalten**und dann auf **Ausblenden** klicken. Anstatt auf die Größe eines Symbols verkleinert zu werden, wird das Fenster in diesem Fall unsichtbar. Verwenden Sie den Befehl **Einblenden** im gleichen Menü, damit das Fenster wieder angezeigt wird. Mithilfe der **AusführenMenübefehl** -Aktion können Sie jeden dieser Befehle auch in einem Makro ausführen.

  - Sie können auch die **SetzenWert** -Aktion verwenden, um die **Sichtbar**-Eigenschaft eines Formulars so festzulegen, dass das Fenster des Formulars ausgeblendet oder angezeigt wird.

Verwenden Sie die **Minimize** -Methode des **DoCmd** -Objekts, um die **MinimierenFenster** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

