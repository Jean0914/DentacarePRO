# DentaCare Pro para iOS (SwiftUI)

Versión nativa de iPhone/iPad de la app web `dental-clinic` (React). Mismos módulos, mismos datos de ejemplo y mismas credenciales demo.

## Requisitos
- Mac con **Xcode 15 o superior** (iOS 17 como mínimo)
- Para iPhone físico: Apple ID (basta la cuenta gratuita), cable y modo desarrollador activado

## Opción A: crear el proyecto a mano en Xcode (la más segura)
1. Xcode > File > New > Project > **iOS > App** > Next.
2. Product Name: `DentaCarePro`. Interface: **SwiftUI**. Language: **Swift**. Storage: None. Guarda donde quieras.
3. En el navegador de archivos de Xcode, **borra** `ContentView.swift` y `DentaCareProApp.swift` (Move to Trash).
4. Arrastra a Xcode los 13 archivos `.swift` de la carpeta `DentaCarePro/` (marca *Copy items if needed* y tu target).
5. En el target > General > **Minimum Deployments**, pon **iOS 17.0**.
6. Elige un simulador (por ejemplo iPhone 15) arriba y pulsa **Run (▶)**, o Cmd+R.

## Opción B: con XcodeGen
    brew install xcodegen
    xcodegen generate
    open DentaCarePro.xcodeproj

## En un iPhone físico
1. Conecta el iPhone, desbloquéalo y toca «Confiar».
2. En el iPhone: Ajustes > Privacidad y seguridad > **Modo de desarrollador** > activar (reinicia).
3. Xcode > target > **Signing & Capabilities** > marca *Automatically manage signing* y elige tu Team (tu Apple ID). Si el identificador ya está en uso, cambia el Bundle Identifier.
4. Elige tu iPhone como destino y pulsa Run. La primera vez, en el iPhone: Ajustes > General > VPN y gestión de dispositivos > confía en tu perfil.

## Credenciales demo
| Rol | Correo | Contraseña |
|---|---|---|
| Dentista/Admin | dentista@clinica.mx | 1234 |
| Paciente | maria.garcia@email.com | 1234 |
| Paciente | carlos.h@email.com | 1234 |

## Cambios respecto a la versión web
- Los datos se guardan como JSON en la carpeta Documents de la app (antes: localStorage). Las imágenes dentales se guardan como archivos JPG ahí mismo.
- El menú lateral pasó a pestañas inferiores (en el panel del dentista, las pestañas extra aparecen bajo «Más»). El cierre de sesión está en el ícono de persona de cada pantalla.
- Las imágenes se eligen de la fototeca (no se admite `.dcm`).
- La gráfica de ingresos mensuales usa los mismos datos de ejemplo que la web (solo el último mes suma los ingresos de hoy).
- Los recibos se pueden compartir como texto con el botón de compartir.

## Aviso
Es una demo: las contraseñas están en texto plano dentro de los datos y no hay cifrado. No la uses con datos reales de pacientes sin añadir autenticación y almacenamiento seguro.
