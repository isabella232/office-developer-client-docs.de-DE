---
title: Kennzeichnen von Geschäftsobjekten als sicher für Skripting
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 942864f1461cc99bd087204cd8c27fc478cb7600
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602241"
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

\<*MyActiveXGUID*\>gibt die hexadezimale GUID-Nummer des Geschäftsobjekts an. Speichern Sie sie, und führen Sie sie mithilfe des Registrierungs-Editors in Ihrer Registrierung zusammen, oder doppelklicken Sie im Explorer Windows auf die REG-Datei.

In Microsoft Visual Basic erstellte Geschäftsobjekte können mit dem Paket- und Bereitstellungs-Assistenten automatisch als "sicher für Skripts" gekennzeichnet werden. Wählen Sie **Safe for initialization** und **Safe for scripting** aus, wenn Sie vom Assistenten auffordert werden, Sicherheitseinstellungen anzugeben.

Im letzten Schritt erstellt der Anwendungseinrichtungs-Assistent eine HTM- und eine CAB-Datei. Sie können diese beiden Dateien anschließend auf den Zielcomputer kopieren. Doppelklicken Sie dann auf die HTM-Datei, um die Seite zu laden und den Server ordnungsgemäß zu registrieren.

Da das Geschäftsobjekt standardmäßig im Windows \\ System32 Occache-Verzeichnis installiert wird, verschieben Sie es in \\ das Windows \\ System32-Verzeichnis, und ändern Sie den **Registrierungsschlüssel HKEY \_ CLASSES ROOT \_ \\ CLSID \\** \<*MyActiveXGUID*\> \\ **InprocServer32** so, dass er dem richtigen Pfad entspricht.


> [!NOTE]
> [!HINWEIS] Geschäftsobjekte, die für die Verwendung von Skript oder für die Initialisierung als sicher gekennzeichnet sind, können von jedem Benutzer über das Netzwerk instanziiert und initialisiert werden. Benutzerdefinierte Geschäftsobjekte dürfen nicht unbedacht entworfen und implementiert werden. Es ist absolut notwendig, dass diese Objekte kein Sicherheitsrisiko darstellen und Hacker durch sie keinen Zugriff auf den vertraulichen Bereich des Hostservers erlangen und Schaden verursachen können.


