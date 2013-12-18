# DialogFragmentBuilder
## usage

    public class HogeFragment extends Fragment implements AlertDialogFragment.Callbacks {
        @Override
        public void onActivityCreated(Bundle savedInstanceState) {
            /*
               some code...
            */
            AlertDialogFragmentBuilder builder = new AlertDialogFragment.Builder();
            builder.setTitle("foo").setMessage("bar");
                    .setViewFromResource(R.layout.baz);
                    .setPositiveButtonLabel(R.string.label_ok);
                    .setNegativeButtonLabel(R.string.label_cancel);
                    .setTargetFragment(this, 0);
                    .create().show(getFragmentManager(), "alert_dialog");
            /*
               some code...
            */
        }

        /*
            some methods...
        */

        @Override
        public void onDialogClicked(DialogInterface dialog, int which) {
            // some code when a button in the dialog is clicked.
        }

        @Overide
        public void onDialogCanceled(DialogInterface dialog) {
            // some code when the dialog is canceled.
        }
    }

## version history

- 12/18/13 Initial commit

