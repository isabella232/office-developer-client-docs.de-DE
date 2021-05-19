---
title: COM (Component Object Model) und MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334468"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) und MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Windows-SDK-Dokumentation enthält eine umfassende Diskussion der Regeln für die Implementierung von Objekten, die dem Component Object Model (COM) entsprechen. Diese Regeln gehen wie folgt vor:
  
- Entwerfen von Schnittstellen und Objekten.
    
- Implementieren Sie [die IUnknown-Schnittstelle.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) 
    
- Verwalten des Arbeitsspeichers.
    
- Behandeln der Verweiszählung.
    
- Implementieren von Objekten mit Apartmentthread.
    
Obwohl alle MAPI-Objekte als COM-basiert betrachtet werden, da sie Schnittstellen implementieren, die von [IUnknown erben,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)weicht MAPI in einigen Situationen von den standardmäßigen COM-Regeln ab. Diese Abweichung ermöglicht Entwicklern mehr Flexibilität bei ihren Implementierungen. Eine MAPI-Schnittstelle beschreibt z. B. wie jede COM-Schnittstelle einen Vertrag zwischen dem Implementier und dem Anrufer. Nachdem die Schnittstelle erstellt und veröffentlicht wurde, kann und ändert sich ihre Definition nicht mehr. MAPI weicht nicht von dieser Beschreibung ab, aber es lockert die Beschreibung etwas. Implementierer können bestimmte Methoden nicht implementieren und einen der folgenden Fehlerwerte an den Aufrufer zurückgeben: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Die anderen Abweichungen von den standardmäßigen COM-Regeln werden in der folgenden Tabelle beschrieben.
  
|**COM-Programmierregel**|**MAPI-Variation**|
|:-----|:-----|
|Alle Zeichenfolgenparameter in Schnittstellenmethoden sollten Unicode sein.  <br/> |MAPI-Schnittstellen sind so definiert, dass sie Unicode- oder ANSI-Zeichenfolgenparameter zulassen. Viele Methoden mit einem Zeichenfolgenparameter verfügen auch über einen **ulFlags-Parameter.** die Breite eines Zeichenfolgenparameters wird durch den Wert des MAPI_UNICODE in **ulFlags angegeben.** Einige MAPI-Schnittstellen unterstützen Unicode nicht und geben MAPI_E_BAD_CHARWIDTH zurück, wenn MAPI_UNICODE festgelegt ist.  <br/> |
|Alle Schnittstellenmethoden sollten den Rückgabetyp HRESULT haben.  <br/> |MAPI verfügt über mindestens eine Methode, die einen Nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Anrufer und Implementierer sollten mithilfe der standardmäßigen COM-Aufgabenzuweisungen Arbeitsspeicher für Schnittstellenparameter zuordnen und frei machen.  <br/> |Alle MAPI-Methoden verwenden die verknüpften Zuweisungen [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) zum Verwalten des Arbeitsspeichers für Schnittstellenparameter. Alle MAPI-Implementierungen von von OLE definierten Schnittstellen, z. B. [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)verwenden die standardmäßigen COM-Aufgabenzuordnungen.  <br/> |
|Alle out-Zeigerparameter müssen explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.  <br/> |FÜR MAPI-Schnittstellen müssen out-Zeigerparameter entweder auf NULL festgelegt oder unverändert bleiben, wenn eine Methode fehlschlägt. Bei allen MAPI-Implementierungen von schnittstellen, die von OLE definiert wurden, werden die Parameter bei einem Fehler explizit auf NULL festgelegt.  <br/> |
|Implementieren Sie nach Möglichkeit aggregierbare Objekte.  <br/> |MAPI-Schnittstellen sind nicht aggregierbar.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

