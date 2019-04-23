---
title: Kennzeichnen von Geschäftsobjekten als sicher für Skripting
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289777"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a>Kennzeichnen von Geschäftsobjekten als sicher für Skripting

**Gilt für**: Access 2013, Office 2013

Sie müssen jedes Geschäftsobjekt, das mit der [CreateObject](dataspace-object-rds.md)-Methode des [RDS.DataSpace](createobject-method-rds.md)-Objekts instanziiert wird, als "Sicher für Skripts" kennzeichnen, um eine möglichst sichere Internetumgebung zu erreichen. Vergewissern Sie sich, dass die Objekte im Lizenzbereich der Systemregistrierung entsprechend gekennzeichnet sind, damit sie in DCOM verwendet werden können.

Wenn Sie ein Geschäftsobjekt manuell als sicher für Skript kennzeichnen möchten, erstellen Sie eine Textdatei mit der Erweiterung REG, die den folgenden Text enthält. Mit den folgenden beiden Nummern wird das Feature für eine sichere Verwendung von Skript aktiviert:

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

dabei \<ist *MyActiveXGUID* \> die hexadezimale GUID-Nummer Ihres Geschäftsobjekts. Speichern Sie es, und führen Sie es mithilfe des Registrierungs-Editors in Ihre Registrierung ein, oder Doppelklicken Sie in Windows Explorer auf die reg-Datei.

Geschäftsobjekte, die in Microsoft Visual Basic erstellt wurden, können mit dem Paket-und Bereitstellungs-Assistenten automatisch als "sicher für die Skripterstellung" gekennzeichnet werden. Wählen Sie **Safe for initialization** und **Safe for scripting** aus, wenn Sie vom Assistenten auffordert werden, Sicherheitseinstellungen anzugeben.

Im letzten Schritt erstellt der Anwendungseinrichtungs-Assistent eine HTM- und eine CAB-Datei. Sie können diese beiden Dateien anschließend auf den Zielcomputer kopieren. Doppelklicken Sie dann auf die HTM-Datei, um die Seite zu laden und den Server ordnungsgemäß zu registrieren.

Da das\\Geschäftsobjekt standardmäßig im Windows System32\\Occache-Verzeichnis installiert wird, verschieben Sie es in das Windows\\System32-Verzeichnis, und ändern Sie die HKEY **\_-Klassen\_-Stamm\\-CLSID\\ ** . \< ** MyActiveXGUID\>InprocServer32-Registrierungsschlüssel zur Übereinstimmung mit dem richtigen Pfad.**** \\


> [!NOTE]
> [!HINWEIS] Geschäftsobjekte, die für die Verwendung von Skript oder für die Initialisierung als sicher gekennzeichnet sind, können von jedem Benutzer über das Netzwerk instanziiert und initialisiert werden. Benutzerdefinierte Geschäftsobjekte dürfen nicht unbedacht entworfen und implementiert werden. Es ist absolut notwendig, dass diese Objekte kein Sicherheitsrisiko darstellen und Hacker durch sie keinen Zugriff auf den vertraulichen Bereich des Hostservers erlangen und Schaden verursachen können.


