---
title: COM (Component Object Model) und MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bfeedf5073e162744099a22b8febcd8fb544da54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567739"
---
# <a name="component-object-model-and-mapi"></a>COM (Component Object Model) und MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Windows SDK-Dokumentation enthält eine umfassende Erläuterung der Regeln für die Implementierung von Objekten, die dem Component Object Model (COM) entsprechen. Diese Regeln behandeln folgende Vorgehensweisen:
  
- Entwerfen sie Schnittstellen und Objekte.
    
- Implementieren Sie die [IUnknown-Schnittstelle.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) 
    
- Verwalten des Arbeitsspeichers.
    
- Behandeln der Referenzzählung.
    
- Implementieren von Apartmentthreadobjekten.
    
Obwohl alle MAPI-Objekte als COM-basiert gelten, da sie Schnittstellen implementieren, die von [IUnknown erben,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)weicht die MAPI in einigen Situationen von den standardmäßigen COM-Regeln ab. Diese Abweichung ermöglicht Entwicklern mehr Flexibilität bei ihren Implementierungen. Beispielsweise beschreibt eine MAPI-Schnittstelle wie jede COM-Schnittstelle einen Vertrag zwischen Implementierer und Aufrufer. Sobald die Schnittstelle erstellt und veröffentlicht wurde, kann und ändert sich ihre Definition nicht. Die MAPI weicht nicht von dieser Beschreibung ab, aber die Beschreibung wird etwas gelockert. Implementierer können festlegen, dass bestimmte Methoden nicht implementiert werden sollen, wobei einer der folgenden Fehlerwerte an den Aufrufer zurückgegeben wird: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Die anderen Abweichungen von den COM-Standardregeln werden in der folgenden Tabelle beschrieben.
  
|**COM-Programmierregel**|**MAPI-Variation**|
|:-----|:-----|
|Alle Zeichenfolgenparameter in Schnittstellenmethoden sollten Unicode sein.  <br/> |MAPI-Schnittstellen sind so definiert, dass unicode- oder ANSI-Zeichenfolgenparameter zulässig sind. Viele Methoden mit einem Zeichenfolgenparameter haben auch einen **ulFlags-Parameter;** Die Breite eines Zeichenfolgenparameters wird durch den Wert des MAPI_UNICODE Flags in **ulFlags** angegeben. Einige MAPI-Schnittstellen unterstützen Unicode nicht und geben MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag festgelegt ist.  <br/> |
|Alle Schnittstellenmethoden sollten einen Rückgabetyp von HRESULT aufweisen.  <br/> |MAPI verfügt über mindestens eine Methode, die einen Nicht-HRESULT-Wert zurückgibt: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Aufrufer und Implementierer sollten Speicher für Schnittstellenparameter mithilfe der standardmäßigen COM-Aufgabenzuweisungen zuordnen und freigeben.  <br/> |Alle MAPI-Methoden verwenden die verknüpften Zuleitungen [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) zum Verwalten des Arbeitsspeichers für Schnittstellenparameter. Alle MAPI-Implementierungen von von OLE definierten Schnittstellen, z. [B. IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)verwenden die standardmäßigen COM-Aufgabenzuweisungen.  <br/> |
|Alle Ausgabezeigerparameter müssen explizit auf NULL festgelegt werden, wenn eine Methode fehlschlägt.  <br/> |MAPI-Schnittstellen erfordern, dass Ausgabezeigerparameter entweder auf NULL festgelegt werden oder unverändert bleiben, wenn eine Methode fehlschlägt. Alle MAPI-Implementierungen von Schnittstellen, die von OLE definiert werden, legen Parameter bei Einem Fehler explizit auf NULL fest.  <br/> |
|Implementieren Sie nach Möglichkeit aggregierbare Objekte.  <br/> |MAPI-Schnittstellen können nicht aggregierbar sein.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

