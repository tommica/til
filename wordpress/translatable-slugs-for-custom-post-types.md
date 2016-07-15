# Translatable slugs for custom post types

```php
/*
    In your register function you can overwrite the slug by doing this:

    $cptName = 'cptsinglularname';
    $slug = get_option( 'wpse3333_'.cptName.'_baseslug' );
    $slug = !$slug ? 'default' : $slug;

    // register your post type, reference $slug for the rewrite
    $args['rewrite']['slug'] = $slug;

    register_post_type('cptname', $args);
*/


add_action( 'load-options-permalink.php', 'wpse3333_load_permalinks' );
function wpse3333_load_permalinks()
{
    $cptName = 'cptsinglularname';

    if( isset( $_POST['wpse3333_'.$cptName.'_baseslug'] ) )
    {
        update_option( 'wpse3333_'.$cptName.'_baseslug', sanitize_title_with_dashes( $_POST['wpse3333_'.$cptName.'_baseslug'] ) );
    }

    // Add a settings field to the permalink page
    add_settings_field( 'wpse3333_'.$cptName.'_baseslug', __( $cptName.' Base', 'textdomain' ), 'wpse3333_field_callback', 'permalink', 'optional' );
}

function wpse3333_field_callback()
{
    $cptName = 'cptsinglularname';

    $value = get_option( 'wpse3333_'.$cptName.'_baseslug' );
    echo '<input type="text" value="' . esc_attr( $value ) . '" name="wpse3333_'.$cptName.'_baseslug" id="wpse3333_'.$cptName.'_baseslug" class="regular-text" placeholder="cptsinglularname" />';
}
```
