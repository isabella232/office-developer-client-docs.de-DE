---
title: Bereitstellen signierter InfoPath-Formularvorlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Informationen zur Sicherheit signierter Formularvorlagen finden Sie unterSigned Form Templatessection in Additional InfoPath Form Security Concepts. Die Informationen und Hinweise im Thema Security Levels, E-Mail Deployment, and Remote Form Templates sind ebenfalls wichtig.
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426800"
---
# <a name="deploying-signed-infopath-form-templates"></a>Bereitstellen signierter InfoPath-Formularvorlagen

Informationen zur Sicherheit signierter Formularvorlagen finden Sie im Abschnitt "Signierte Formularvorlagen" unter [Zusätzliche InfoPath-Formularsicherheitskonzepte.](additional-infopath-form-security-concepts.md) Die Informationen und Hinweise im Thema [Security Levels, E-Mail Deployment, and Remote Form Templates](security-levels-email-deployment-and-remote-form-templates.md) sind ebenfalls wichtig. 
  
## <a name="digitally-signing-a-form-template"></a>Digitales Signieren einer Formularvorlage

Wenn Sie eine Formularvorlage digital signieren, können Sie die Sicherheitsstufe für die Formularvorlage auf Voll vertrauenswürdig festlegen, was bedeutet, dass das Formular auf Dateien und Einstellungen auf dem Computer des Benutzers oder in einer anderen Domäne zugreifen kann. (Das digitale Signieren einer Formularvorlage verhindert auch nicht, dass Sie andere Sicherheitsstufen verwenden, wenn Sie dies bevorzugen. Sie legen die Sicherheitsstufe einer signierten Formularvorlage auf die Sicherheitsstufe "Domäne" oder "Eingeschränkt" festgelegt.) Darüber hinaus können Sie die signierte Formularvorlage für Benutzer bereitstellen, die ein E-Mail-Programm verwenden, und dann die signierte Formularvorlage später automatisch aktualisieren, indem Sie die aktualisierte Version als Anlage an eine E-Mail-Nachricht an die Benutzer senden, führen Sie die folgenden Schritte aus:
  
### <a name="to-digitally-sign-a-form-template"></a>So können Sie eine Formularvorlage digital signieren

1. Klicken Sie im InfoPath-Designer auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
2. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**. 
    
3. Aktivieren Sie unter **Signatur der Formularvorlage** das Kontrollkästchen **Diese Formularvorlage signieren**. 
    
4. Klicken Sie auf **Zertifikat auswählen**.
    
5. Klicken Sie im Dialogfeld **Zertifikat auswählen** auf das Zertifikat, mit dem Sie das Formular digital signieren möchten. 
    
> [!NOTE]
> Mit der Schaltfläche **Zertifikat erstellen** im Dialogfeld **Formularoptionen** kann ein Testzertifikat zum Signieren einer Formularvorlage generiert werden. Das Testzertifikat sollte nur zu Testzwecken zum Signieren von Formularvorlagen verwendet werden. Mit Testzertifikaten sollten keine Formularvorlagen signiert werden, die öffentlich weitergegeben werden. Die Zertifikate werden nicht von einer Zertifizierungsstelle ausgestellt, deren Stammzertifikat bereits auf dem Computer eines Benutzers vertrauenswürdig ist, weshalb die Testzertifikate auf dem Computer des Benutzers nicht ordnungsgemäß überprüft werden. Wenn Sie eine mit einem Testzertifikat signierte Formularvorlage bereitstellen, können Benutzer Ihrer Formularvorlage diese höchstwahrscheinlich nicht öffnen. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Einrichten eines vertrauenswürdigen Stammzertifikats und eines vertrauenswürdigen Herausgebers

  Das vertrauenswürdige Stammzertifikat des Zertifikats, mit dem die Formularvorlage signiert wird, muss im Speicher für vertrauenswürdige Stammzertifikate auf dem Clientcomputer vorhanden sein. Andernfalls kann der Herausgeber der Formularvorlage nicht überprüft werden, und Benutzer Ihrer Formularvorlage haben nicht die Möglichkeit, dem Herausgeber zu vertrauen. Falls sich das vertrauenswürdige Stammzertifikat im Speicher für vertrauenswürdige Stammzertifikate befindet, aber der Herausgeber nicht in der Liste vertrauenswürdiger Herausgeber vorhanden ist, werden die Benutzer aufgefordert bzw. haben die Möglichkeit, dem Herausgeber der Formularvorlage zu vertrauen. 
  
> [!NOTE]
> Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, überprüft InfoPath mithilfe der Signatur, ob die Formularvorlage nach dem Signieren manipuliert wurde. Außerdem bestimmt InfoPath mithilfe der Signatur, ob die Formularvorlage automatisch aktualisiert werden kann. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Bereitstellen signierter Formularvorlagen mit der Sicherheitsstufe "Voll vertrauenswürdig"

Das primäre Szenario für die Bereitstellung signierter Formularvorlagen besteht in der Aktivierung domänen like-funktionalität, z. B. der automatischen Aktualisierung, in vollständig vertrauenswürdigen Formularen. Eine signierte Formularvorlage, die voll vertrauenswürdigen Zugriff anfordert, hat denselben Zugriff auf Systemressourcen wie ein *voll vertrauenswürdiges Formular.* Eine ausführliche Erläuterung der Funktionsweise voll vertrauenswürdiger Formulare und wie sie erstellt und bereitgestellt werden finden Sie unter [Grundlegendes zu voll vertrauenswürdigen Formularen](understanding-fully-trusted-forms.md).
  
In Abhängigkeit von der EDV-Umgebung Ihrer Organisation ziehen Sie jedoch möglicherweise die Verwendung signierter Formularvorlagen oder voll vertrauenswürdiger Formulare vor. Beispielsweise bietet die Verwendung einer signierten Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, anstelle eines registrierten, voll vertrauenswürdigen Formulars die folgenden Vorteile:
  
- Im Gegensatz zu einer unsignierten, voll vertrauenswürdigen Formularvorlage ist keine Registrierung erforderlich.
    
- Die automatische Aktualisierung der Formularvorlage ist möglich.
    
Da eine signierte Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, keine Registrierung erfordert, müssen Sie diese nicht mit einem Installer-Paket oder einer Skriptdatei bereitstellen. Dadurch wird die Bereitstellung einer voll vertrauenswürdigen Formularvorlage erheblich vereinfacht.
  
Beim Aktualisieren der signierten Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, können Sie einfach die aktualisierte Vorlage an den Benutzer senden oder diese in einem freigegebenen Speicherort aktualisieren. Wenn der Benutzer die aktualisierte Vorlage öffnet, wird der Benutzer nicht aufgefordert, und die ältere Kopie auf dem Computer des Benutzers wird automatisch mit der aktualisierten Version überschrieben. Falls Sie die Vorlage in einem freigegebenen Speicherort aktualisiert haben, kann der Benutzer die aktualisierte Kopie ohne Bestätigung verwenden.
  
Falls Sie ein unsigniertes, voll vertrauenswürdiges Formular aktualisieren möchten, müssen Sie das Formular erneut packen und registrieren. Darüber hinaus kann eine vorhandene und installierte voll vertrauenswürdige Formularvorlage nur für den Pfad des lokalen Computers, nicht aber für einen Netzwerkpfad verwendet werden, da für den Registrierungsvorgang ein lokaler Computerpfad nicht in einen Netzwerkpfad geändert werden kann. Da allerdings ein Zertifikat zum Signieren einer Formularvorlage erforderlich ist, sollten Sie eventuell voll vertrauenswürdige, registrierte Formularvorlagen bereitstellen, wenn Sie kein Zertifikat erwerben möchten.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Bereitstellen signierter Formularvorlagen mit der Domänensicherheitsstufe oder der eingeschränkten Sicherheitsstufe 

Eine signierte Formularvorlage mit der Domänensicherheitsstufe oder der eingeschränkten Sicherheitsstufe bietet außerdem den Vorteil der automatischen Aktualisierungsfunktion. Beispielsweise können Sie eine signierte Formularvorlage in einer Dokumentbibliothek auf einem Server mit Microsoft SharePoint Foundation oder auf einem Server mit Domänensicherheitsstufe veröffentlichen. Wenn Sie Ihre Formularvorlage in dem freigegebenen Speicherort aktualisieren, erhalten die Benutzer automatisch die aktualisierte Kopie.
  

