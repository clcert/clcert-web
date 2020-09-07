
---
title: "Estudio: Al menos 2.972 servidores de correo electrónico Exim en Chile afectados por severa vulnerabilidad."
author: CLCERT Universidad de Chile.
image: /img/posts/old_mailbox.jpg
date: "2019-06-14 13:21:20"
summary: "Como parte de nuestras labores usuales de monitoreo, esta semana detectamos la existencia de al menos 2.972 servidores de correo vulnerables visibles en la Internet chilena. Estos servidores corren versiones 4.87 a 4.91 del manejador de correo Exim el cual es [altamente vulnerable](https://www.exim.org/static/doc/security/CVE-2019-10149.txt)."
---
Como parte de nuestras labores usuales de monitoreo, esta semana detectamos la existencia de al menos 2.972 servidores de correo vulnerables visibles en la Internet chilena. Estos servidores corren versiones 4.87 a 4.91 del manejador de correo Exim el cual es [altamente vulnerable](https://www.exim.org/static/doc/security/CVE-2019-10149.txt). En concreto, un atacante podría ejecutar comandos en forma remota en el [servidor](https://www.qualys.com/2019/06/05/cve-2019-10149/return-wizard-rce-exim.txt). Se recomienda a todos aquellos afectados actualizar **lo antes posible** a una versión más reciente, pues ya se han detectado [varios ataques](https://twitter.com/freddieleeman/status/1137729455181500421) [en curso](https://www.cybereason.com/blog/new-pervasive-worm-exploiting-linux-exim-server-vulnerability).

[Más detalles técnicos aquí](https://nvd.nist.gov/vuln/detail/CVE-2019-10149).

Los detalles de los servidores afectados fueron compartidos con el CSIRT del Gobierno de Chile, organización que está analizando los datos. Se recomienda a los administradores de redes que sospechan pudieran estar afectadas contactarse directamente con esta entidad, al teléfono +(562) 2486 3850 o directamente en [el sitio web del CSIRT del Gobierno de Chile](https://www.csirt.gob.cl/).

_Alejandro Hevia_

_Académico del Departamento de Ciencias de la Computación de la Facultad de Ciencias Físicas y Matemáticas de la Universidad de Chile, y Director del Laboratorio de Seguridad Computacional y Criptografía Aplicada CLCERT._
