---
title: Office für Android-Unterstützung für Android Storage Access Framework
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office für Android lässt sich in Android Storage Access Framework integrieren, mit dem Office Dateien öffnen kann, die von einem anderen Dokumentanbieter gespeichert werden.
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790894"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a>Office für Android-Unterstützung für Android Storage Access Framework

Office für Android lässt sich in Android Storage Access Framework integrieren, mit dem Office Dateien öffnen kann, die von einem anderen Dokumentanbieter gespeichert werden.
  
In Android 4.4 (API Level 19) wird das Storage Access Framework (SAF) eingeführt. Mit SAF können Benutzer Dokumente, Bilder und andere Dateien durchsuchen und öffnen, die von den bevorzugten Dokumentspeicheranbieter gespeichert sind. Mit der Standard-Benutzeroberfläche können Benutzer Dateien auf konsistente Weise App- und Anbieter-übergreifend durchsuchen und auf diese zugreifen.
  
## <a name="implement-a-document-provider"></a>Implementieren eines Dokumentanbieters

Wenn Sie eine App entwickeln, die Speicherdienste für Dokumente bereitstellt, können Sie Ihre Dateien über SAF durch [Schreiben eines benutzerdefinierten Dokumentanbieters](https://developer.android.com/guide/topics/providers/document-provider.html) zur Verfügung stellen. Office-Apps können dann die [ACTION_OPEN_DOCUMENT ](https://developer.android.com/reference/android/content/Intent.html)- und/oder [ACTION_CREATE_DOCUMENT ](https://developer.android.com/reference/android/content/Intent.html)-Absicht zum Empfangen der Dateien aufrufen, die von Ihrem Dokumentanbieter zurückgegeben wurden. Beachten Sie, dass die Absicht Filter zum weiteren Verfeinern der Kriterien enthalten kann. 
  
## <a name="enable-free-consumer-edits"></a>Aktivieren der kostenlosen Bearbeitung

Benutzer können sich mit einem kostenlosen Microsoft-Konto bei Office-Apps anmelden, um Dokumente zu erstellen oder zu bearbeiten, die in einem benutzerorientierten Speicherdienst gespeichert sind. In der folgenden Tabelle werden die obligatorischen Eigenschaften aufgeführt, die Anbieter im Rahmen des Cursors bereitstellen müssen, um die kostenlose Bearbeitung der über das Storage Access Framework zugegriffenen Dokumenten zu ermöglichen.
  
|**Eigenschaft**|**Index**|**Wert**|
|:-----|:-----|:-----|
|Dokumenttyp  <br/> |com_microsoft_office_doctype  <br/> |\<Benutzer\>  <br/> |
|Anzeigename des Dienstes  <br/> |com_microsoft_office_servicename  <br/> |Ein beliebiger benutzerfreundlicher Name für den Dienst, der zum Identifizieren eines Dokuments in der Liste der zuletzt geöffneten Dokumente in Office-Apps verwendet wird. Beachten Sie, dass die Eigenschaft für Lizenzbedingungen angegeben werden muss, bevor der Anzeigename für den Dienst angezeigt werden kann.  <br/> |
|Nutzungsbedingungen  <br/> |com_microsoft_office_termsofuse  <br/> |\<Ich stimme den Bedingungen befindet sich unterhttp://go.microsoft.com/fwlink/p/?LinkId=528381\>  <br/> |
   
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Integration in Office](integrate-with-office.md)
    
- [Grundlagen für Inhaltsanbieter](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [Erstellen eines Inhaltsanbieters](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [Storage Access Framework - Entwicklerhandbuch](https://developer.android.com/guide/topics/providers/document-provider.html)
    

